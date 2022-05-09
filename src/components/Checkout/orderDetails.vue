<template>
  <div class="container">
   <h3 class="order-details">Your Order</h3>
   <div class="main-container flex-property">
    <label for="product" class="product">PRODUCT</label>
     <!-- <label for="product" class="total">TOTAL</label> -->
   </div>
  </div>
</template>

<script>

export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main-container{
  /* display: flex; */
}
.order-details{
  display: flex;
  font-size: 26px;
  line-height: 35px;
  color: #000000;
}
.flex-property{
  display: flex;
}
.total{
  flex-direction: row-reverse;
}
</style>
