<template>
  <div class="container">
    <div class="header">
      <div class="logoContainer">
        <img src="../../assets/SHOPPE.svg" />
      </div>
      <div class="linksContainer">
        <a href="#">Shop</a>
        <a href="#">Blog</a>
        <a href="#">Our Story</a>
        <img src="../../assets/line.png" class="line" />
        <a href="#"><img src="../../assets/search.png" /></a>
        <a href="#"><img src="../../assets/cart.png" /></a>
        <a href="#"><img src="../../assets/profile.png" /></a>
      </div>
    </div>
    <hr class="divider" />
  </div>
</template>

<script>
export default {
  name: "ShoppeHeader",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  padding: 15px 70px;
}
.logoContainer {
  width: 50%;
  display: flex;
  align-items: baseline;
}
.linksContainer {
  width: 50%;
  display: flex;
  justify-content: space-evenly;
  align-items: baseline;
}
.header {
  display: flex;
  
}
.line {
  padding-left: 40px;
}
.divider {
  margin: 15px 0px;
  color:#D8D8D8;
}
a {
  text-decoration: none;
  color: #000000;
  padding-left: 60px;
}
</style>
