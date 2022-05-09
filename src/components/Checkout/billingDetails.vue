<template>
  <div class="main-container">
    <h3 class="billing-header">Billing details</h3>
    <div class="info-fill">
      <form action="">
        <div class="full-name">
          <div class="coupon name">
            <label class="couponlabel" for="couponcode">First name*</label>
            <input type="texr" />
          </div>
          <div class="coupon name">
            <label class="couponlabel" for="couponcode">Last name*</label>
            <input type="text" />
          </div>
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">Company name</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">Country*</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">Street address*</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">Postal code/zip*</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">Town/city*</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">Phone*</label>
          <input type="text" />
        </div>
        <div class="coupon">
          <label class="couponlabel" for="couponcode">Email*</label>
          <input type="text" />
        </div>
        <div class="checkbox">
          <div class="create-acc  flex-property">
            <input type="checkbox" name="account" id="" />
            <label for="acc">Create an account?</label>
          </div>
         
          <div class="ship  flex-property">
            <input type="checkbox" name="account" id="" />
            <label for="acc">Ship to a different address</label>
          </div>
        </div>
        <div class="coupon email">
          <label class="couponlabel" for="couponcode">Other notes</label>
          <input type="text" />
        </div>
      </form>
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
   padding-left: 9.6rem;
  
}
.billing-header {
  display: flex;
  font-size: 26px;
  line-height: 35px;
  color: #000000;
}
.coupon input {
  outline: none;
  /* width: 100%; */
 
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #d8d8d8;
}
.couponlabel {
  display: flex;
  font-size: 12px;
  color: #707070;
}
.flex-property {
  display: flex;
}
.name {
  padding-right: 2rem;
}
.full-name {
  display: grid;
  grid-auto-flow: column;
}
.coupon {
  padding-top: 3.2rem;
}
.checkbox{
    padding-top: 2rem;
}
.ship{
    padding-top: 1rem;
}
.email{
    padding-bottom: 2rem;
}
</style>
