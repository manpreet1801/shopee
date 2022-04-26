<template>
  <div class="home">
    <img class="img" src="../assets/Img1.svg" alt="" />
    <div class="product-label">
      <div id="labelName">Gold Big Hoops</div>
      <div id="price">$68.00</div>
      <button class="button">View Product</button>
    </div>
    <div class="view">
      <div id="label">Shop The Latest</div>
      <a href="" id="viewAll">View All</a>
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
  /* margin: 10px 0px 0px 96px; */
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
.product-label {
  position: absolute;
  top: 200px;
  left: 150px;
  color: white;
}
.button {
  border: 2px solid white;
  border-radius: 5px;
  color: white;
  background-color: transparent;
  margin-top: 3rem;
  font-size: 20px;
  padding: 13px 30px 14px 30px;
}
#labelName {
  font-size: 3rem;
}
#price {
  font-size: 2rem;
  margin-top: 10px;
}
#viewAll {
  color: #a18a68;
  border: none;
}
.img {
  width: 100%;
}
</style>
