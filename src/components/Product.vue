<template>
    <div class="product">
        <div class="container">
            <div class="product__nav">
                <h2 class="title">Popular <span class="title-span">Products</span></h2>
                <ul class="product__list">
                    <li class="product__item">
                        <button @click="tabIndex = 1" :class="tabIndex == 1 ? 'active' : ''">All</button>
                    </li>
                    <li class="product__item">
                        <button @click="tabIndex = 2" :class="tabIndex == 2 ? 'active' : ''">Milks</button>
                    </li>
                    <li class="product__item">
                        <button @click="tabIndex = 3" :class="tabIndex == 3 ? 'active' : ''">Pet Foods</button>
                    </li>
                    <li class="product__item">
                        <button @click="tabIndex = 4" :class="tabIndex == 4 ? 'active' : ''">Vegetables</button>
                    </li>
                    <li class="product__item">
                        <button @click="tabIndex = 5" :class="tabIndex == 5 ? 'active' : ''">Fruits</button>
                    </li>
                </ul>
            </div>
            <div class="product__cards" v-if="tabIndex == 1">
                <div class="product__card" v-for="product in productObj">
                    <div class="hot" :class="product.line == 'hot' ? 'active' : ''">
                        <p>Hot</p>
                    </div>
                    <div class="hot2" :class="product.line == 'hot2' ? 'active' : ''">
                        <p>Hot</p>
                    </div>
                    <div class="product__image">
                        <span>
                            <font-awesome-icon :icon="['fas', 'heart']" />
                        </span>
                        <img :src="product.image" alt="">
                    </div>
                    <div class="product__card-footer">
                        <p>Category</p>
                        <h4>{{ product.name }}</h4>
                        <div class="product__card-stars">
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon style="color: #939393;" :icon="['fas', 'star']" />
                        </div>
                        <div class="product__card-price">
                           <div>
                               <p>Piker per kg</p>
                               <p class="price">
                                  <span>{{ product.price }}</span>
                                  <del>{{ product.previous }}</del>
                               </p>
                           </div>
                           <button>
                               <font-awesome-icon :icon="['fas', 'cart-shopping']" />
                               <span>add</span>
                           </button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="product__cards" v-if="tabIndex == 2">
                <div class="product__card"  v-for="product in productObj2">
                    <div class="hot" :class="product.line == 'hot' ? 'active' : ''">
                        <p>Hot</p>
                    </div>
                    <div class="hot2" :class="product.line == 'hot2' ? 'active' : ''">
                        <p>Hot</p>
                    </div>
                    <div class="product__image">
                        <span>
                            <font-awesome-icon :icon="['fas', 'heart']" />
                        </span>
                        <img :src="product.image" alt="">
                    </div>
                    <div class="product__card-footer">
                        <p>Category</p>
                        <h4>{{ product.name }}</h4>
                        <div class="product__card-stars">
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon :icon="['fas', 'star']" />
                            <font-awesome-icon style="color: #939393;" :icon="['fas', 'star']" />
                        </div>
                        <div class="product__card-price">
                           <div>
                               <p>Piker per kg</p>
                               <p class="price">
                                  <span>{{ product.price }}</span>
                                  <del>{{ product.previous }}</del>
                               </p>
                           </div>
                           <button>
                               <font-awesome-icon :icon="['fas', 'cart-shopping']" />
                               <span>add</span>
                           </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { reactive, ref } from 'vue';

// const productItemBtn = reactive(['All','Milks','Pet Foods','Vegetables','Fruits'])
const tabIndex = ref(1);


const productObj = reactive([
    {
        image: '../../public/image/products/pngwing4.svg',
        name: 'Garbuz Ukraine',
        price: '$24.00',
        previous: '$30.00',
        line: 'hot'
    },
    {
        image: '../../public/image/products/pngwing5.svg',
        name: 'Ground allspice',
        price: '$29.00',
        previous: '$32.00',
        
    },
    {
        image: '../../public/image/products/pngwing6.svg',
        name: 'Wash the carot',
        price: '$22.00',
        previous: '$28.00'
    },
    {
        image: '../../public/image/products/pngwing7.svg',
        name: 'Boston',
        price: '$20.00',
        previous: '$33.00',
        line: 'hot2'
    },
    {
        image: '../../public/image/products/pngwing9.svg',
        name: 'Petya Zhovta',
        price: '$26.00',
        previous: '$34.00'
    },
    {
        image: '../../public/image/products/pngwing10.svg',
        name: 'Boby Edamame c/m',
        price: '$23.00',
        previous: '$32.00',
        line: 'hot2'
    },
    {
        image: '../../public/image/products/pngwing11.svg',
        name: 'Kiwi Gold',
        price: '$28.00',
        previous: '$28.00',
        line: 'hot'
    },
    {
        image: '../../public/image/products/pngwing12.svg',
        name: 'Mushhroom Shiitake',
        price: '$29.00',
        previous: '$28.00',
        line: 'hot'
    },
])
const productObj2 = reactive([
    {
        image: '../../public/image/products/pngwing5.svg',
        name: 'Garbuz Ukraine',
        price: '$24.00',
        previous: '$30.00',
        line: 'hot'
    },
    {
        image: '../../public/image/products/pngwing4.svg',
        name: 'Ground allspice',
        price: '$29.00',
        previous: '$32.00',
        
    },
    {
        
        image: '../../public/image/products/pngwing9.svg',
        name: 'Wash the carot',
        price: '$22.00',
        previous: '$28.00',
        line: 'hot2'
    },
    {
        image: '../../public/image/products/pngwing12.svg',
        name: 'Petya Zhovta',
        price: '$20.00',
        previous: '$33.00',
    },
    {
        image: '../../public/image/products/pngwing7.svg',
        name: 'Boston',
        price: '$26.00',
        previous: '$34.00',
        line: 'hot2'
    },
    {
        image: '../../public/image/products/pngwing11.svg',
        name: 'Boby Edamame c/m',
        price: '$23.00',
        previous: '$32.00',
        line: 'hot'
    },
    {
        image: '../../public/image/products/pngwing10.svg',
        name: 'Kiwi Gold',
        price: '$28.00',
        previous: '$28.00',
        line: 'hot2'
    },
    {
        image: '../../public/image/products/pngwing6.svg',
        name: 'Mushhroom Shiitake',
        price: '$29.00',
        previous: '$28.00',
        line: 'hot'
    },
])
</script>

<style lang="scss" scoped>
.product {
    margin-bottom: 80px;
    .container {
        .product__nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 40px;
            .title {
                margin: 0;
            }
            .product__list {
                display: flex;
                column-gap: 20px;
                .product__item {
                    button {
                        font-size: 20px;
                        color: var(--link);
                        transition: .5s;
                        &.active {
                            color: var(--link-hover);
                        }
                        &:hover {
                            color: var(--link-hover);
                        }
                    }
                }
            }
        }
        .product__cards {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            row-gap: 30px;
            .product__card {
                position: relative;
                max-width: 269px;
                width: 100%;
                border: 1px solid var(--border);
                border-radius: 10px;
                padding: 23px;
                transition: .5s;
                overflow: hidden;
                cursor: pointer;
                &:hover {
                    box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.1);
                }
                .hot {
                    position: absolute;
                    top: 7px;
                    left: -36px;
                    width: 130px;
                    background: #67BCEE;
                    color: var(--white);
                    padding: 10px 0;
                    text-align: center;
                    transform: rotate(-40deg);
                    display: none;
                    &.active {
                        display: block;
                    }
                }
                .hot2 {
                    position: absolute;
                    top: 7px;
                    left: -36px;
                    width: 130px;
                    background: #F74B81;
                    color: var(--white);
                    padding: 10px 0;
                    text-align: center;
                    transform: rotate(-40deg);
                    display: none;
                    &.active {
                        display: block;
                    }
                }
                .product__image {
                    position: relative;
                    min-height: 210px;
                    margin-bottom: 42px;
                   span {
                       position: absolute;
                       right: 0;
                       color: var(--link);
                       font-size: 20px;
                       z-index: 11;
                       &:hover {
                        color: #F74B81;
                       }
                   }
                   img {
                    position: absolute;
                    max-width: 208px;
                    min-height: 210px;
                   }
                   
                }
                .product__card-footer {
                    p {
                        font-size: 13px;
                        color: var(--link);
                        font-weight: 500;
                    }
                    h4 {
                        font-size: 20px;
                        color: var(--text);
                        font-weight: 600;
                        margin: 10px 0;
                    }
                    .product__card-stars {
                        color: var(--star);
                        display: flex;
                        column-gap: 5px;
                        font-size: 25px;
                    }
                    .product__card-price {
                        margin-top: 20px;
                        display: flex;
                        align-items: center;
                        justify-content: space-between;
                        div {
                            .price {
                                margin-top: 8px;
                                span {
                                    font-size: 16px;
                                    color: var(--text);
                                    font-weight: 700;
                                }
                            }
                        }
                        button {
                            display: flex;
                            column-gap: 10px;
                            background: #D4EEE2;
                            padding: 10px;
                            border-radius: 5px;
                            color: #2FD080;
                            text-transform: capitalize;
                        }
                    }
                }
            }
        }
    }
}
</style>