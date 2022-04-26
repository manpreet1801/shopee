<template>
  <div class="home">
    <img src="../assets/Img1.svg" alt="" />
    <div class="view">
      <div id="label">Shop The Latest</div>
      <div>View all</div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from "./footer.vue";
export default {
  name: "homePage",
  components: {
    Footer,
  },
};
</script>

<style scoped>
.home {
  margin: 10px 0px 0px 96px;
}
#label {
  font-weight: 600;
  font-size: 33px;
}
.view {
  justify-content: space-between;
  margin-top: 60px;
  display: flex;
}
</style>
