<template>
  <div id="app">
    <shopee/>
  </div>
</template>

<script>
import shopee from './components/shopee.vue'

export default {
  name: 'App',
  components: {
    shopee
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
