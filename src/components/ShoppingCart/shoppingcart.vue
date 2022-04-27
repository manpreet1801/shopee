<template>
  <div>
    <h2 class="header">Shopping cart</h2>
    <div class="container left">
      <leftSide />
    </div>
    <div class="container right">
      <rightSide />
    </div>
  </div>
</template>

<script>
import leftSide from "./leftSide.vue";
import rightSide from "./rightSide.vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components: {
    leftSide,
    rightSide,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.right {
  right: 0;
}
.left {
  left: 0;
}
.container {
  /* top: 0; */
  display: flex;
  height: 100%;
  width: 50%;
  position: fixed;
  z-index: 1;
  overflow-x: hidden;
  padding-top: 20px;
  padding-left: 9.6rem;
}
.header {
  color: #000000;
}
.details {
  margin-left: 0;
  margin-right: 0;
  margin-top: 0;
  margin-bottom: auto;
   width: max-content;
  padding-left: 16px;
}
.price {
  padding-top: 8px;
}
.img {
  margin-left: 0;
  margin-right: 0;
  margin-top: auto;
  margin-bottom: auto;
  padding-right: 16px;
}
.sub-container {
  display: flex;
  padding-bottom: 10px;
  padding-top: 10px;
}
.split {
  height: 100%;
  width: 50%;
  position: fixed;
  z-index: 1;
  top: 0;
  overflow-x: hidden;
  padding-top: 20px;
}
.item-name {
  display: flex;
  font-weight: bold;
  margin-bottom: 0.9rem;
}
.size {
  margin-left: 0;
}
.price {
  display: flex;
  color: #a18a68;
}
.logo {
  height: 100px;
  width: 100px;
}
.btn {
  border: none;
  padding-top: 2px;
  margin: 4px;
  padding-bottom: 2px;
}
.quantity {
  padding-left: 8.4rem;
}
.delete {
  padding-left: 2rem;
}
.cross-sign {
  height: 12px;
  width: 11.82px;
}
</style>
