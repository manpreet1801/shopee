<template>
  <div class="main">
    <h2 class="heading">Checkout</h2>
    <div class="conatiner">
      <span class="customer">Returning Customer?</span
      ><span>Click here to login</span>
    </div>
    <div class="conatiner">
      <span class="customer">Have Coupon?</span
      ><span>Click here to enter your code</span>
    </div>
    <div class="container-box">
      <div>
        <span class="text flex-property"
          >If you have a coupon code please apply it below.</span
        >
      </div>

      <div class="updateCart-btn coupon-btn flex-property">
        <div class="coupon flex-property">
          <label class="couponlabel flex-property" for="couponcode"
            >coupon code</label
          >
          <input type="text" />
          <div class="btn">
            <button class="applyCouponBtn">APPLY COUPON</button>
          </div>
        </div>
      </div>
    </div>
    <div class="split left-side">
      <billingDetails />
    </div>
    <div class="split right-side">
      <orderDetails />
    </div>
  </div>
</template>

<script>
import orderDetails from "../Checkout/orderDetails.vue";
import billingDetails from "./billingDetails.vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components: {
    billingDetails,
    orderDetails,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main {
  padding-left: 9.6rem;
  /* padding-right: 9.6rem; */
}
.heading {
  font-weight: 500;
  font-size: 33px;
  line-height: 43px;
  color: #000;
}
.customer {
  color: #707070;
  padding-right: 8px;
}
.conatiner {
  display: flex;
  padding-bottom: 2.4rem;
}
.coupon {
  padding-top: 2rem;
}
.coupon input {
  outline: none;
  border: none;
  border-bottom: 1px solid #d8d8d8;
}
.couponlabel {
  font-size: 12px;
  color: #707070;
}
.flex-property {
  display: flex;
}
.updateCart-btn {
  display: flex;
}
.applyCouponBtn {
  font-size: 10px;
  height: 53px;
   border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
  background-color: #000000;
  color: #ffff;
  font-weight: 700;
  font-size: 16px;
}
.container-box {
  border-style: solid;
  border: 1px solid #d8d8d8;
  width: 30%;
  padding: 2rem;
}
.btn {
  padding-left: 1rem;
}
.split {
  /* display: flex; */
  height: 100%;
  width: 50%;
  position: absolute;
}
.right-side {
  right: 0;
}
.left-side {
  left: 0;
}
</style>
