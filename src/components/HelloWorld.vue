<template>
  <div>
    <div id="main">
      <section class="hero">
        <h1 class="heading">George Kirby</h1>
        <h3 class="subheading">Web designer & developer</h3>
      </section>
      <section class="intro">
        Full stack (front-end?) web developer (and designer) with a love of
        using technology to simplify life’s everyday tasks. After tackling a
        variety of roles, I have found my place in programming’s thoughtful
        problem-solving. I’m now striving to work in a small team with open
        communication, where I can keep learning quickly and deepen my skills.
      </section>
      <section class="tech-skills">
        <h2>Technical Skills</h2>
        <p>Vue, ?React, JavaScript, HTML, CSS, ?Rails, ?Ruby, ?SQL</p>
        <!-- card for each tech, with logo, ?proficiency -->
      </section>
      <section class="projects">
        <h2>Projects</h2>
        <!-- card for each project -->
        <div class="project-cards-container">
          <div class="project-card"></div>
          <div class="project-card"></div>
          <div class="project-card"></div>
        </div>
      </section>
      <section class="experience">
        <h2>Experience</h2>
        <!-- card for each experience -->
        <div class="experience-cards-container">
          <div class="experience-card"></div>
          <div class="experience-card"></div>
          <div class="experience-card"></div>
        </div>
      </section>
      <section class="interests">
        <h2>Interests</h2>
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
export default {
  name: "HelloWorld",
  data() {
    return {
      showTips: false,
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
  background-image: url("../../src/assets/freelance-stock-image.jpg");
  background-size: cover;
  background-position: center;

  display: grid;
  grid-template-columns: 1fr 10px 300px 10px 1fr;
  grid-template-rows: 1fr 20px 10px 20px 40px;
  grid-template-areas:
    ". . . . ."
    ". . heading . ."
    ". . . . ."
    ". . subheading . ."
    ". . . . .";

  color: white;
  text-align: left;
}

.hero .heading {
  grid-area: heading;
  font-size: 25px;
}

.hero .subheading {
  grid-area: subheading;
  font-size: 16px;
}

div#vueTips {
  margin-top: 100px;
}
</style>
