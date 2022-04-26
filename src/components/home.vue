<template>
  <div class="home">
    <img class="img" src="../assets/Img1.svg" alt="" />
    <div class="product-label">
      <div id="labelName">Gold Big Hoops</div>
      <div id="price">$68.00</div>
      <button class="button">View Product</button>
    </div>
    <div class="view">
      <div id="label">Shop The Latest</div>

      <a href="" id="viewAll">View All</a>
    </div>
    <div class="product-list">
      <productCard
        v-for="product in products"
        :product="product"
        :key="product.id"
      />
    </div>
    <Footer />
  </div>
</template>

<script>
import prod1 from "../assets/product-1.svg";
import prod2 from "../assets/product-2.svg";
import prod3 from "../assets/product-3.svg";
import prod4 from "../assets/product-4.svg";
import prod5 from "../assets/product-5.svg";
import prod6 from "../assets/product-6.svg";
import Footer from "./footer.vue";
import productCard from "./productCard.vue";

export default {
  name: "homePage",
  components: {
    Footer,
    productCard,
  },
  data() {
    return {
      products: [
        {
          id: "p1",
          name: "Lira Earrings",
          price: 20.0,
          isInStock: true,
          image: prod1,
          showLabel: false,
        },
        {
          id: "p2",
          name: "Hal Earrings",
          price: 25.0,
          isInStock: true,
          image: prod2,
          showLabel: false,
        },
        {
          id: "p3",
          name: "Kaede Hair Pin Set Of 3",
          price: 30.0,
          isInStock: true,
          image: prod3,
          showLabel: false,
        },
        {
          id: "p4",
          name: "Hair Pin Set Of 3",
          price: 30.0,
          isInStock: true,
          image: prod4,
          showLabel: false,
        },
        {
          id: "p5",
          name: "Plaine Necklace",
          price: 19.0,
          isInStock: true,
          image: prod5,
          showLabel: false,
        },
        {
          id: "p6",
          name: "Yuki Hair Pin Set of 3",
          price: 29.0,
          isInStock: false,
          image: prod6,
          showLabel: false,
        },
      ],
    };
  },
};
</script>

<style scoped>
.home {
  /* margin: 10px 0px 0px 96px; */
  width: 100%;
}
#label {
  font-weight: 600;
  font-size: 33px;
}
.view {
  justify-content: space-between;
  margin-top: 60px;
  display: flex;
}
.product-label {
  position: absolute;
  top: 200px;
  left: 150px;
  color: white;
}
.product-list {
  display: flex;
  flex-wrap: wrap;
  flex: 1;
  gap: 1.25rem;
  margin-top: 30px;
}
.button {
  border: 2px solid white;
  border-radius: 5px;
  color: white;
  background-color: transparent;
  margin-top: 3rem;
  font-size: 20px;
  padding: 13px 30px 14px 30px;
}
#labelName {
  font-size: 3rem;
}
#price {
  font-size: 2rem;
  margin-top: 10px;
}
#viewAll {
  color: #a18a68;
  border: none;
}
.img {
  width: 100%;
}
</style>
