<template>
  <div id="app">
    <!-- <header></header> -->
    <Home />
  </div>
</template>

<script>

import Home from "./components/home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style>
#app {
  margin: auto 70px;
}
</style>
