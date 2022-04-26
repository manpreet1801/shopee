<template>
    <div>
        <div class="shop-container">
            <div class="shop-filters">
                <h1 class="shop-heading">Shop The Latest</h1>
                <div class="search-input-wrapper"><input class="search-input" name="search" type="text" placeholder="Search" /></div>
                <div class="shop-by-dropdown">
                    <select>
                        <option>Shop By</option>
                    </select>
                </div>
                <div class="sort-by-dropdown">
                    <select>
                        <option>Sort By</option>
                    </select>
                </div>
                <div class="on-sale-wrapper toggle-button-wrapper">
                    <label for="on-sale">On sale</label>
                    <toggle-button v-model="fileterOnSale" color="#707070" switch-color="#FFFFFF" :sync="true" width="33.33" height="20" />
                </div>
                <div class="in-stock-wrapper toggle-button-wrapper">
                    <label for="in-stock">In stock</label>
                    <toggle-button v-model="filterInStock" color="#707070" switch-color="#FFFFFF" :sync="true" width="33.33" height="20" />
                </div>
            </div>
            <div class="product-list">
                <productCard v-for="product in products" :product="product" :key="product.id" />
            </div>
        </div>
        <footerComp />
    </div>
</template>

<script>
import prod1 from '../assets/product-1.svg';
import prod2 from '../assets/product-2.svg';
import prod3 from '../assets/product-3.svg';
import prod4 from '../assets/product-4.svg';
import prod5 from '../assets/product-5.svg';
import prod6 from '../assets/product-6.svg';

import productCard from './productCard.vue';
import footerComp from './footer.vue';

export default {
    name: 'ShopPage',
    components: {
        productCard,
        footerComp,
    },
    method: {},
    data() {
        return {
            fileterOnSale: false,
            filterInStock: true,
            products: [
                {
                    id: 'p1',
                    name: 'Lira Earrings',
                    price: 20.0,
                    hasDiscount: true,
                    discount: 21,
                    isInStock: true,
                    image: prod1,
                },
                {
                    id: 'p2',
                    name: 'Hal Earrings',
                    price: 25.0,
                    hasDiscount: false,
                    discount: 0,
                    isInStock: true,
                    image: prod2,
                },
                {
                    id: 'p3',
                    name: 'Kaede Hair Pin Set Of 3',
                    price: 30.0,
                    hasDiscount: false,
                    discount: 0,
                    isInStock: true,
                    image: prod3,
                },
                {
                    id: 'p4',
                    name: 'Hair Pin Set Of 3',
                    price: 30.0,
                    hasDiscount: false,
                    discount: 0,
                    isInStock: true,
                    image: prod4,
                },
                {
                    id: 'p5',
                    name: 'Plaine Necklace',
                    price: 19.0,
                    hasDiscount: false,
                    discount: 0,
                    isInStock: false,
                    image: prod5,
                },
                {
                    id: 'p6',
                    name: 'Yuki Hair Pin Set of 3',
                    price: 29.0,
                    hasDiscount: false,
                    discount: 0,
                    isInStock: true,
                    image: prod6,
                },
            ],
        };
    },
};
</script>

<style scoped>
.shop-container {
    /* max-width: 1280px; */
    display: flex;
    gap: 2.25rem;
    /* margin-inline: auto;
    padding-inline: 1rem; */
}
.shop-filters {
    flex: 0 0 270px;
}
.product-list {
    display: flex;
    flex-wrap: wrap;
    gap: 1.25rem;
    flex: 1;
}
.shop-heading {
    font-weight: 500;
    font-size: 33px;
    line-height: 43px;
    margin-bottom: 40px;
}
select {
    width: 100%;
    border: 1px solid #d8d8d8;
    font-weight: 100;
    font-size: 14px;
    padding: 15px 12px;
}
.search-input {
    width: 100%;
    outline: 0;
    border: 0;
    border-bottom: 1px solid #d8d8d8;
    padding-bottom: 11px;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
}
.search-input-wrapper {
    position: relative;
    margin-bottom: 2.437rem;
}
.search-input-wrapper::after {
    display: block;
    content: '';
    background-image: url('../assets/search-icon.svg');
    position: absolute;
    right: 0;
    top: 0;
    height: 20px;
    width: 20px;
}
.shop-by-dropdown {
    margin-bottom: 1rem;
}
.on-sale-wrapper {
    margin-top: 2.625rem;
    margin-bottom: 2.625rem;
}
.toggle-button-wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>
