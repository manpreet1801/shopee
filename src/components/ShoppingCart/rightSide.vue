<template>
  <div>
    <h4 class="header">Cart Totals</h4>
    <div class="sub-total">
      <label class="subtotal">SUBTOTAL</label>
      <label class="subtotal subTotal">$65.00</label>
    </div>
    <div class="flex-property shipping">
      <label class="subtotal">SHIPPING</label>
      <div class="values">
        <label class="flex-property subtotalValue shippingValue"
          >shipping cost will be calculated<br />once you have provided address.
        </label>
        <div class="flex-property calculate"><h6>CALCULATE SHIPPING</h6></div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">SELECT COUNTRY</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">CITY</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">POSTAL CODE/ZIP</label>
          <input type="text" />
        </div>
        <div class="updateBtn">
          <button class="update">UPDATE TOTALS</button>
        </div>
      </div>
    </div>
    <hr class="divider" />
    <div class="flex-property totalValues">
      <label class="total" for="">TOTAL</label>
      <label class="flex-property totalAmt" for="">$87.00</label>
    </div>
    <div class="proceedBtn">
      <button class="checkout">PROCEED TO CHECKOUT</button>
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
.subtotal {
  font-weight: 400;
  font-size: 16px;
  line-height: 27px;
  padding-left: 1.5rem;
}
.coupon input {
  outline: none;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #d8d8d8;
}
.couponlabel {
  display: flex;
  font-size: 12px;
  color: #707070;
}
h4 {
  display: flex;
  color: #000000;
}
.header {
  padding-left: 1rem;
}

.sub-total {
  display: flex;
}
.subtotal {
  font-weight: 400;
  font-size: 14px;
  line-height: 27px;
}
.subTotal {
  padding-left: 4.8rem;
}

.flex-property {
  display: flex;
}
.values {
  padding-left: 4.8rem;
}
.coupon input {
  outline: none;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #d8d8d8;
}
.coupon {
  padding-bottom: 12px;
}
.couponlabel {
  display: flex;
  font-size: 9px;
  color: #707070;
}
.update {
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
  background: #ffffff;
  font-size: 10px;
  padding: 8px;
  width: 100%;
}
.subtotalValue {
  font-weight: 400;
  font-size: 14px;
  line-height: 27px;
  color: #707070;
}
.totalAmt {
  padding-left: 11.8rem;
  font-weight: bold;
}
.total {
  font-weight: bold;
}
.totalValues {
  padding-top: 4px;
  margin-left: 4rem;
  margin-right: 4rem;
}
.divider {
  margin-left: 4rem;
  margin-right: 3rem;
}
.checkout {
  background: #000000;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
  color: #ffffff;
  padding: 8px;
  font-size: 9px;
  width: 300px;
}
.proceedBtn {
  padding-top: 16px;
}
</style>
