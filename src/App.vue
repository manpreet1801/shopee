<template>
  <div id="app">
    <!-- <shopee/> -->
    <productDetais msg='Prerana Here'/>
  </div>
</template>

<script>
// import shopee from './components/shopee.vue'
import productDetais from './components/productDetails/productDetails.vue'

export default {
  name: 'App',
  components: {
    // shopee,
    productDetais
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
  /* margin-top: 60px; */
}
</style>
