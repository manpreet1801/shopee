<template>
  <div class="product-wrapper">
    <div class="product-img-container">
      <img class="product-image" :src="product.image" />
    </div>
    <div
      class="product-label product-discount"
      v-if="product.showLabel && product.hasDiscount"
    >
      -%{{ product.discount }}
    </div>
    <div
      class="product-label product-stock"
      v-if="product.showLabel && !product.isInStock"
    >
      Sold out
    </div>
    <div class="product-name">
      <h3>{{ product.name }}</h3>
    </div>
    <div class="product-price">
      <h4>$ {{ product.price }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  props: ["product"],
};
</script>

<style scoped>
.product-wrapper {
  position: relative;
}
.product-img-container {
  margin-bottom: 1.5rem;
}
.product-label {
  background-color: #a18a68;
  padding: 2px 8px;
  border-radius: 4px;
  color: #fff;
  position: absolute;
  left: 16px;
  top: 16px;
}
.product-name h3 {
  font-size: 1.25rem;
  font-weight: 400;
  line-height: 26px;
  margin-bottom: 1rem;
}
.product-price h4 {
  font-style: normal;
  font-weight: 500;
  font-size: 1.25rem;
  line-height: 26px;
  text-transform: capitalize;
  color: #a18a68;
}
</style>
