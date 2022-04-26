<template>
    <div class="shop-container">
        <div class="shop-filters">
            <h1 class="shop-heading">Shop The Latest</h1>
            <div><input class="search-input" name="search" type="text" placeholder="Search" /></div>
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
            <div class="on-sale-wrapper">
                <label for="on-sale">On sale</label>
                <input id="on-sale" name="on-sale" type="checkbox" class="toggle" />
            </div>
            <div class="in-stock-wrapper">
                <label for="in-stock">In stock</label>
                <input id="in-stock" name="in-stock" type="checkbox" class="toggle" />
            </div>
        </div>
        <div class="product-list">
            <productCard v-for="product in products" :product="product" :key="product.id" />
        </div>
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
export default {
    name: 'ShopPage',
    components: {
        productCard,
    },
    data() {
        return {
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
    max-width: 1440px;
    display: flex;
    gap: 2.25rem;
    margin-inline: auto;
    padding-inline: 6rem;
}
.shop-filters {
    flex: 0 0 270px;
}
.product-list {
    display: flex;
    flex-wrap: wrap;
    flex: 1;
    gap: 1.25rem;
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
    margin-bottom: 2.437rem;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    position: relative;
}
.search-input::after {
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

input[type='checkbox'].toggle {
    opacity: 0;
    position: absolute;
    left: -9000px;
    /* top: -9000px; */
}

input[type='checkbox'].toggle + label {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;
    font-weight: 400;
    font-size: 16px;
    line-height: 27px;
}

input[type='checkbox'].toggle + label::after {
    content: '';
    width: 2em;
    height: 1em;
    background-color: hsl(0, 80%, 90%);
    border-radius: 1em;
    margin-right: 0.25em;
    transition: background-color 200ms ease-in-out;
}

/* input[type='checkbox'].toggle + label::before {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    content: '\2715';
    font-size: 0.5em;
    height: 0.9em;
    left: 0.2em;
    width: 1.8em;
    height: 1.8em;
    background-color: hsl(0, 80%, 60%);
    color: white;
    border-radius: 1em;
    transition: background-color 200ms ease-in-out, transform 200ms ease-in-out;
} */

/* input[type='checkbox'].toggle:focus + label::before {
    outline: 1px solid black;
} */

/* input[type='checkbox'].toggle:checked + label::before {
    background-color: hsl(100, 70%, 90%);
} */

/* input[type='checkbox'].toggle:checked + label::before {
    content: '\2713';
    transform: translateX(100%);
    background-color: hsl(100, 70%, 60%);
} */

/* input[type='checkbox'].toggle:disabled + label {
    color: #777;
} */

/* input[type='checkbox'].toggle:disabled + label::before {
    background-color: #ccc;
}

input[type='checkbox'].toggle:disabled + label::after {
    background-color: #777;
} */
</style>
