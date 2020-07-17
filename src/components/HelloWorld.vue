<template>
  <div>
    <div id="main">
      <section class="hero">
        <div class="content">
          <h1 class="heading">George Kirby</h1>
          <h3 class="subheading">Full stack software engineer</h3>
        </div>
      </section>
      <div id="main-body">
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
              <img
                class="logo"
                :src="skill.logoPath"
                :alt="skill.alt"
              />
            </div>
          </div>
        </section>
        <section class="projects">
          <h2>Projects</h2>
          <p>card for each project</p>
          <!-- card for each project -->
          <div class="project-cards-container">
            <div class="project-card"></div>
            <div class="project-card"></div>
          </div>
        </section>
      </div>
      <section class="experience">
        <h2>Experience</h2>
        <p>card for each experience</p>
        <!-- card for each experience -->
        <div class="experience-cards-container">
          <div class="experience-card">
            <div class="inner">
              <div class="front">
                <div class="content">
                  <h3 class="dates">August - November 2019</h3>
                  <p class="role">Software Engineering student</p>
                  <p class="organisation">Flatiron School</p>
                </div>
              </div>
              <div class="back">
                <ul>
                  <li>
                    Rapidly developed skills in a variety of technologies,
                    including React and Rails, during an intense 15-week
                    bootcamp.
                  </li>
                  <li>Built several projects in focused one-week sprints.</li>
                  <li>
                    Engaged in industry practices such as user testing and pair
                    programming.
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="experience-card">
            <div class="inner">
              <div class="front">
                <div class="content">
                  <h3 class="dates">March 2018 - July 2019</h3>
                  <p class="role">Teaching Assistant</p>
                  <p class="organisation">
                    Chapel End Junior Academy / Lathom Junior School, London
                  </p>
                </div>
              </div>
              <div class="back">
                <ul>
                  <li>
                    Provided in-class support to low-attaining Year 6 children.
                  </li>
                  <li>
                    Prepared and delivered own lessons to small focus groups in
                    reading, arithmetic and handwriting.
                  </li>
                  <li>
                    After SATs, worked 1-to-1 with SEN children, providing
                    academic, emotional and physical support.
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="experience-card">
            <div class="inner">
              <div class="front">
                <div class="content">
                  <h3 class="dates">October 2017 - February 2018</h3>
                  <p class="role">Warehouse Assistant</p>
                  <p class="organisation">
                    A Warne & Co, London
                  </p>
                </div>
              </div>
              <div class="back">
                <ul>
                  <li>
                    Worked in a plastics factory, moving flexibly between
                    different roles as demand required.
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <!-- <div class="experience-card"></div>
          <div class="experience-card"></div> -->
        </div>
      </section>
      <section class="interests">
        <h2>Interests</h2>
        <p>card for each interest</p>
        <!-- card for each interest -->
        <div class="interest-cards-container">
          <div class="interest-card"></div>
          <div class="interest-card"></div>
          <div class="interest-card"></div>
        </div>
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
import { techSkills } from "../content/TechSkills";

export default {
  name: "HelloWorld",
  data() {
    return {
      showTips: false,
      techSkills,
    };
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
  display: inline-block;
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
}

.experience-card {
  height: 170px;
  width: 300px;
  background-color: transparent;
  margin: 10px;
}

.experience-card .inner {
  position: relative;
  height: 100%;
  width: 100%;
  /* border: solid 1px black; */
  transition: transform 0.5s;
  transform-style: preserve-3d;
}

.experience-card:hover .inner {
  transform: rotateY(180deg);
}

.experience-card .front,
.experience-card .back {
  position: absolute;
  height: 100%;
  width: 100%;
  backface-visibility: hidden;
}

.experience-card .front {
  background: white;
}

.experience-card .front .content {
  width: 220px;
  margin: 40px auto;
}

.experience-card .back {
  background: white;
  transform: rotateY(180deg);
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

  div#main-body {
    display: grid;
    grid-template-columns: 1fr 450px 50px 200px 1fr;
    grid-template-rows: 30px 250px 30px 250px 30px;
    grid-template-areas:
      ". . . . ."
      ". intro . skills ."
      ". . . skills ."
      ". projects . skills ."
      ". . . . .";
  }

  section.intro {
    grid-area: intro;
    margin: 0;
  }

  section.skills {
    grid-area: skills;
  }

  section.projects {
    grid-area: projects;
  }
}
</style>
