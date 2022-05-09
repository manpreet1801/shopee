<template>
  <div>
    <applyCoupon />
  </div>
</template>

<script>
import applyCoupon from "./applyCoupon.vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components: {
    applyCoupon,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
