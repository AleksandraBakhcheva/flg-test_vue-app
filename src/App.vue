<template>
  <HomePage />
</template>

<script>
import HomePage from "./views/HomePage.vue";

export default {
  name: "App",
  components: {
    HomePage,
  },
};
</script>

<style>
@import url(https://necolas.github.io/normalize.css/latest/normalize.css);

* {
  margin: 0;
  padding: 0;
}

body {
  max-width: 1400px;
  margin: 0 auto;
}

#app {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
  box-sizing: border-box;
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000000;
  background-color: #e5e5e5;
}
</style>
