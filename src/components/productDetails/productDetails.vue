<template>
  <div>
    <Header />
    <div class="product_container">
      <div>
        <div v-for="item in EARING_IMAGES" :key="item.id">
          <img :src="require(`../../assets/${item.images}`)" class="images" />
        </div>
      </div>
      <div>
        <img src="../../assets/Img.svg" />
        <hr class="line_padding" />
      </div>
      <div class="info">
        <h1>Lira Earrings</h1>
        <h4>$ 20,00</h4>
        <div class="rate_container">
          <div v-for="item in RATE_ICON" :key="item.id">
            <img :src="require(`../../assets/${item.icon}`)" class="rate" />
          </div>
          <span>1 customer review</span>
        </div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi
          eaque tempora corporis, ducimus, est sed, nisi natus quis corrupti
          dignissimos iure. Laborum quas omnis impedit est voluptatum quis totam
          incidunt.
        </p>

        <button class="btn-border">-</button>
        <button class="btn-border">1</button>
        <button class="btn-border">+</button>
        <button class="addToCart">Add To Cart</button>
        <div class="icon_container">
          <div v-for="item in SOCIAL_ICONS" :key="item.id">
            <img :src="require(`../../assets/${item.icon}`)" class="icon" />
          </div>
        </div>
        <div v-for="item in JEWELLERY_INFO" :key="item.id" class="list">
          {{ item.title }}: <span class="desc">{{ item.desc }}</span>
        </div>
      </div>
    </div>
    <div class="navBar">
    <div class="linksContainer">
      <a href="#">Description</a>
      <a href="#">Aditional information</a>
      <a href="#">Reviews(0)</a>
    </div>
    <hr/>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus
      dolore, totam ab voluptates tempore possimus repellat rem delectus dolores
      adipisci, voluptas architecto porro distinctio earum impedit hic odio
      quibusdam sed.
    </p>
    </div>
    <div>
      <h2>Similar Items</h2>
      <div class="similar_products">
        <div v-for="item in SIMILAR_ITEMS" :key="item.id">
          <img :src="require(`../../assets/${item.images}`)" />
          <h3>{{ item.title }}</h3>
          <h4>{{ item.price }}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./header.vue";
import {
  EARING_IMAGES,
  JEWELLERY_INFO,
  SOCIAL_ICONS,
  RATE_ICON,
  SIMILAR_ITEMS,
} from "./constants";
export default {
  name: "ProductDetails",
  components: {
    Header,
  },
  data() {
    return {
      EARING_IMAGES,
      JEWELLERY_INFO,
      SOCIAL_ICONS,
      RATE_ICON,
      SIMILAR_ITEMS,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin-top: 0px;
  font-weight: 400;
}
h4 {
  color: #a18a68;
  margin-bottom: 70px;
}
p {
  color: #707070;
  line-height: 27px;
  margin-bottom: 28px;
  text-align: left;
}
h2 {
  text-align: left;
  margin-left: 70px;
  margin-top: 90px;
}
button {
  padding: 15px 15px;
}
a {
  text-decoration: none;
  color: #000000;
  padding-right: 60px;
}
.linksContainer {
  display: flex;
  align-items: baseline;
  margin-top: 90px;
  margin-bottom: 35px;
}
.product_container {
  display: flex;
  text-align: left;
  padding: 15px 70px;
}
.image_container {
  display: flex;
  flex-direction: column;
}
.images {
  height: 120px;
  width: 120px;
  border-radius: 10px;
  margin: 0px 40px 40px 0px;
  display: flex;
  flex-direction: column;
}
.icon_container {
  display: flex;
  margin-top: 80px;
  margin-bottom: 50px;
}
.info {
  padding-left: 64px;
  justify-self: start;
}
.list {
  margin-top: 15px;
}
.rate_container {
  display: flex;
}
.rate {
  padding-right: 10px;
}
.btn-border {
  border: none;
}
.addToCart {
  margin-left: 23px;
  padding: 15px 100px;
  border: 1px #000000 solid;
  border-radius: 4px;
  background: #ffffff;
  text-transform: uppercase;
}
.icon {
  margin-right: 23px;
}
.desc {
  color: #707070;
  padding-left: 4px;
}
.line_padding {
  margin-top: 24px;
}
.similar_products {
  display: flex;
  justify-content: space-evenly;
  text-align: left;
}
.navBar{
  padding-right: 70px;
  padding-left: 70px;
}
</style>
