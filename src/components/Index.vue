<template>
  <div>
    <div id="main">
      <section class="hero">
        <div class="content">
          <h1 class="heading">George Kirby</h1>
          <h3 class="subheading">Full stack software engineer</h3>
        </div>
      </section>
      <div id="at-a-glance">
        <section class="contact">
          <!-- icon for each -->
          <div class="email">{{ contact.email }}</div>
          <div class="mobile-number">{{ contact.mobile }}</div>
          <div class="github">{{ contact.github }}</div>
        </section>
        <section class="intro">
          Full stack (front-end?) web developer (and designer) with a love of
          using technology to simplify life’s everyday tasks. After tackling a
          variety of roles, I have found my place in programming’s thoughtful
          problem-solving. I’m now striving to work in a small team with open
          communication, where I can keep learning quickly and deepen my skills.
        </section>
        <section class="skills">
          <h2>Technical Skills</h2>
          <!-- Vue, ?React, JavaScript, HTML, CSS, ?Rails, ?Ruby, ?SQL -->
          <!-- card for each tech, with logo, ?proficiency -->
          <div class="skill-cards-container">
            <div
              v-for="skill in techSkills"
              :key="skill.name"
              class="skill-card"
            >
              <p>{{ skill.name }}</p>
              <img class="logo" :src="skill.logoPath" :alt="skill.alt" />
            </div>
          </div>
        </section>
      </div>
      <section class="projects">
        <h2>Projects</h2>
        <p>card for each project</p>
        <!-- card for each project -->
        <div class="project-cards-container">
          <div class="project-card"></div>
          <div class="project-card"></div>
        </div>
      </section>
      <section class="experience">
        <h2>Experience</h2>
        <!-- card for each experience -->
        <div class="experience-cards-container">
          <div
            v-for="role in experience"
            :key="role.title"
            class="experience-card"
            :class="{
              active: isActive(role.title),
              long: role.bullets.length > 1,
            }"
            v-on:click="toggleActive(role.title)"
          >
            <div class="summary">
              <h3 class="dates">{{ role.dates }}</h3>
              <p class="role">{{ role.title }}</p>
              <p class="organisation">{{ role.organisation }}</p>
            </div>
            <div class="detail">
              <ul>
                <li v-for="(bullet, i) in role.bullets" :key="i">
                  {{ bullet }}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>
      <section class="interests">
        <h2>Interests</h2>
        <p>
          In my free time, I’m most likely to be found playing football - Sunday
          League is the highlight of my week! Otherwise, I’ll be escaping London
          for some fresh air, buried in a fantasy novel, or catching up with
          friends.
        </p>
      </section>
      <section class="themes"></section>
      <section class="contact"></section>
      <section class="feedback"></section>
    </div>
    <div id="vueTips">
      <button v-on:click="showTips = !showTips">
        {{ showTips ? "Hide Vue tips" : "Show Vue tips" }}
      </button>
      <div v-if="showTips" class="hello">
        <p>
          For a guide and recipes on how to configure / customize this
          project,<br />
          check out the
          <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
            >vue-cli documentation</a
          >.
        </p>
        <h3>Installed CLI Plugins</h3>
        <ul>
          <li>
            <a
              href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel"
              target="_blank"
              rel="noopener"
              >babel</a
            >
          </li>
          <li>
            <a
              href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint"
              target="_blank"
              rel="noopener"
              >eslint</a
            >
          </li>
        </ul>
        <h3>Essential Links</h3>
        <ul>
          <li>
            <a href="https://vuejs.org" target="_blank" rel="noopener"
              >Core Docs</a
            >
          </li>
          <li>
            <a href="https://forum.vuejs.org" target="_blank" rel="noopener"
              >Forum</a
            >
          </li>
          <li>
            <a href="https://chat.vuejs.org" target="_blank" rel="noopener"
              >Community Chat</a
            >
          </li>
          <li>
            <a href="https://twitter.com/vuejs" target="_blank" rel="noopener"
              >Twitter</a
            >
          </li>
          <li>
            <a href="https://news.vuejs.org" target="_blank" rel="noopener"
              >News</a
            >
          </li>
        </ul>
        <h3>Ecosystem</h3>
        <ul>
          <li>
            <a href="https://router.vuejs.org" target="_blank" rel="noopener"
              >vue-router</a
            >
          </li>
          <li>
            <a href="https://vuex.vuejs.org" target="_blank" rel="noopener"
              >vuex</a
            >
          </li>
          <li>
            <a
              href="https://github.com/vuejs/vue-devtools#vue-devtools"
              target="_blank"
              rel="noopener"
              >vue-devtools</a
            >
          </li>
          <li>
            <a
              href="https://vue-loader.vuejs.org"
              target="_blank"
              rel="noopener"
              >vue-loader</a
            >
          </li>
          <li>
            <a
              href="https://github.com/vuejs/awesome-vue"
              target="_blank"
              rel="noopener"
              >awesome-vue</a
            >
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import { contact } from "../content/Contact";
import { techSkills } from "../content/TechSkills";
import { experience } from "../content/Experience";

export default {
  name: "HelloWorld",
  data() {
    return {
      showTips: false,
      contact,
      techSkills,
      experience,
      activeExperiences: [],
    };
  },
  methods: {
    isActive(title) {
      return this.activeExperiences.includes(title);
    },
    toggleActive(title) {
      this.activeExperiences.includes(title)
        ? (this.activeExperiences = this.activeExperiences.filter(
            (el) => el != title
          ))
        : this.activeExperiences.push(title);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}

section.hero {
  min-height: 400px;
  background-image: url("../assets/freelance-stock-image.jpg");
  background-size: cover;
  background-position: center;

  display: grid;
  grid-template-columns: 1fr 15px 300px 15px 1fr;
  grid-template-rows: 1fr 50px 30px;
  grid-template-areas:
    ". . . . ."
    ". . content . ."
    ". . . . .";
  color: white;
  filter: grayscale(1);

  text-align: left;
}

.hero .content {
  grid-area: content;
}

.hero .heading {
  font-size: 25px;
}

.hero .subheading {
  font-size: 16px;
}

div#vueTips {
  margin-top: 100px;
}

section.intro {
  margin: 20px auto;
  padding: 10px;
  max-width: 400px;
}

.skills .skill-card {
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-between;
  width: 160px;
  margin: 5px 0;
}

.skills .skill-card p {
  align-self: center;
  font-weight: bold;
}

.skills .skill-card img.logo {
  width: 50px;
  height: 50px;
}

section.experience {
  background-color: lightblue;
}

.experience-cards-container {
  display: flex;
  flex-wrap: wrap;
}

.experience-card {
  height: 85px;
  width: 280px;
  background-color: white;
  margin: 10px;
  padding: 5px 10px;
  overflow-y: hidden;
  transition: 0.6s;
  cursor: pointer;
}

.experience-card .detail {
  display: none;
}

.experience-card.active {
  height: 160px;
}

.experience-card.active .detail {
  display: block;
}

.experience-card.long.active {
  height: 350px;
}

.experience-card .front {
  background: white;
}

.experience-card .front .content {
  width: 225px;
  margin: 40px auto;
}

.experience-card .front .content p {
  margin: 5px 0;
}

.experience-card .back li {
  list-style: disc;
}

@media screen and (min-width: 500px) {
  section.hero {
    grid-template-rows: 1fr 80px 40px;
  }

  .hero .heading {
    font-size: 35px;
  }

  .hero .subheading {
    grid-area: subheading;
    font-size: 20px;
  }
}

@media screen and (min-width: 900px) {
  section.hero {
    grid-template-columns: 1fr 15px 400px 15px 1fr;

    grid-template-rows: 1fr 110px 1fr;
  }

  .hero .heading {
    font-size: 52px;
    text-align: center;
  }

  .hero .subheading {
    grid-area: subheading;
    font-size: 25px;
    text-align: center;
  }

  div#at-a-glance {
    display: grid;
    grid-template-columns: 1fr 450px 50px 200px 1fr;
    grid-template-rows: 30px 100px 30px 220px 30px;
    grid-template-areas:
      ". . . . ."
      ". contact . skills ."
      ". . . skills ."
      ". intro . skills ."
      ". . . . .";
  }

  section.contact {
    grid-area: contact;
    padding: 10px;
  }

  section.intro {
    grid-area: intro;
    margin: 0;
  }

  section.skills {
    grid-area: skills;
  }
}
</style>
