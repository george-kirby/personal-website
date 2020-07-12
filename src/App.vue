<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <HelloWorld />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

:-webkit-any(article, aside, nav, section) h1 {
  font-size: 1em;
  margin-block-start: 0em;
  margin-block-end: 0em;
}

h2 {
  margin-block-start: 0em;
  margin-block-end: 0em;
}

h3 {
  font-size: 1em;
  margin-block-start: 0em;
  margin-block-end: 0em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  font-weight: bold;
}

body {
  margin: 0px;
}
</style>
