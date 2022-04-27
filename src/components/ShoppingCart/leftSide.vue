<template>
  <div>
    <div class="sub-container">
      <div class="img">
        <img class="logo" src="../../assets/Img 01.png" alt="" />
      </div>

      <div class="details">
        <span class="item-name">Lira Earrings </span>
        <span class="size">Black/Medium</span>
        <span class="price">$20.00</span>
      </div>
      <div class="quantity">
        <button class="btn mainBtn">
          <button class="btn dec"><img src="../../assets/-.png" /></button
          >1<button class="btn inc">
            <img src="../../assets/+.png" />
          </button>
        </button>
      </div>
      <div class="delete">
        <img class="cross-sign" src="../../assets/Vector.png" alt="" />
      </div>
    </div>
    <hr class="border-style" />
    <div class="sub-container">
      <div class="img">
        <img class="logo" src="../../assets/Img 02.png" alt="" />
      </div>

      <div class="details">
        <span class="item-name">Ollie Earrings </span>
        <span class="size">Black/Medium</span>
        <span class="price">$20.00</span>
      </div>
      <div class="quantity">
        <button class="btn mainBtn">
          <button class="btn dec"><img src="../../assets/-.png" /></button
          >1<button class="btn inc">
            <img src="../../assets/+.png" />
          </button>
        </button>
      </div>
      <div class="delete">
        <img class="cross-sign" src="../../assets/Vector.png" alt="" />
      </div>
    </div>
    <hr class="border-style" />
    <div class="sub-container">
      <div class="img">
        <img class="logo" src="../../assets/Img 03.png" alt="" />
      </div>

      <div class="details">
        <span class="item-name">Kaede Hair Pin </span>
        <span class="size">Black/Medium</span>
        <span class="price">$20.00</span>
      </div>
      <div class="quantity">
        <button class="btn mainBtn">
          <button class="btn dec"><img src="../../assets/-.png" /></button
          >1<button class="btn inc">
            <img src="../../assets/+.png" />
          </button>
        </button>
      </div>
      <div class="delete">
        <img class="cross-sign" src="../../assets/Vector.png" alt="" />
      </div>
    </div>
    <hr class="border-style" />
    <div class="updateCart-btn">
      <button class="update-btn">UPDATE CART</button>
    </div>

    <div class="updateCart-btn coupon-btn">
      <button class="applyCouponBtn">APPLY COUPON</button>

      <div class="coupon">
        <label class="couponlabel" for="couponcode">coupon code</label>
        <input type="text" />
      </div>
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
.border-style {
  color: #d8d8d8;
}
.header {
  color: #000000;
 }
.details {
  margin-left: 0;
  margin-right: 0;
  margin-top: 0;
  margin-bottom: auto;
  /* margin: auto; */
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
  height: 80;
  width: 80px;
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
.updateCart-btn {
  display: flex;
  flex-direction: row-reverse;
  padding-bottom: 2rem;
  padding-top: 8px;
  padding-right: 2.5rem;
}
.update-btn {
  margin-left: 6px;
  font-size: 10px;
  height: 33px;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
  background: #ffff;
}
.applyCouponBtn {
  font-size: 10px;
  height: 33px;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
  background-color: #000000;
  color: #ffff;
}
.coupon {
  padding-right: 8rem;
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
</style>
