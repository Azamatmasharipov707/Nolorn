<template>
    <div class="best">
        <div class="container">
            <h2 class="title">Daily<span class="title-span">Best Sells</span></h2>
            <Carousel class="best__slider" :items-to-show="4">
                <slide class="best__slide best__slide-first">
                    <div class="best__slide-card">
                        <h1>A Burst of energy</h1>
                        <Button />
                    </div>
                </slide>
                <slide class="best__slide" v-for="best in bestObj" :key="best">
                    <div class="best__slide-card">
                        <div class="hot" :class="best.line == 'hot' ? 'active' : ''">
                            <p>Hot</p>
                        </div>
                        <div class="hot2" :class="best.line == 'hot2' ? 'active' : ''">
                            <p>Hot</p>
                        </div>
                        <div class="best__image">
                            <span>
                                <font-awesome-icon :icon="['fas', 'heart']" />
                            </span>
                            <img :src="best.image" alt="">
                        </div>
                        <div class="best__slide-footer">
                            <p>Category</p>
                            <h4>{{ best.name }}</h4>
                            <div class="best__slide-stars">
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon style="color: #939393;" :icon="['fas', 'star']" />
                            </div>
                            <div class="best__slide-price">
                               <div>
                                   <p>Piker per kg</p>
                                   <p class="price">
                                      <span>{{ best.price }}</span>
                                      <span>{{ best.previous }}</span>
                                   </p>
                               </div>
                            </div>
                            <button>
                                <font-awesome-icon :icon="['fas', 'cart-shopping']" />
                                <span>Add to Cart</span>
                            </button>
                        </div>
                    </div>
                </slide>

                <template #addons>
                    <navigation />
                </template>
            </Carousel>
        </div>
    </div>
</template>

<script setup>
import Button from './Button.vue';
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import { reactive } from 'vue';

const bestObj = reactive([
    {
        image: '../../public/image/best/gorih-pecan1.svg',
        name: 'Gorih pecan',
        price: '$24.00',
        previous: '$30.00',
        line: 'hot'
    },
    {
        image: '../../public/image/best/gorih-pecan2.svg',
        name: 'Gorih pecan',
        price: '$24.00',
        previous: '$30.00'
    },
    {
        image: '../../public/image/best/gorih-pecan3.svg',
        name: 'Gorih pecan',
        price: '$24.00',
        previous: '$30.00',
        line: 'hot2'
    },
    {
        image: '../../public/image/best/gorih-pecan1.svg',
        name: 'Gorih pecan',
        price: '$24.00',
        previous: '$30.00',
        line: 'hot'
    },
    {
        image: '../../public/image/best/gorih-pecan2.svg',
        name: 'Gorih pecan',
        price: '$24.00',
        previous: '$30.00'
    },
    {
        image: '../../public/image/best/gorih-pecan3.svg',
        name: 'Gorih pecan',
        price: '$24.00',
        previous: '$30.00',
        line: 'hot2'
    },
])
</script>

<style lang="scss" scoped>
.best {
    .container {
        .best__slider {
            .best__slide-first {
                .best__slide-card {
                    justify-content: flex-end !important;
                    background: url(../../public/image/best/Frame\ 30.svg) no-repeat center center / cover;
                    h1 {
                        color: var(--white);
                        font-size: 40px;
                        line-height: 48px;
                        text-align: left;
                        margin-bottom: 30px;
                    }
                }
            }
            .best__slide {
                padding: 30px 0;
                .best__slide-card {
                    max-width: 270px;
                    width: 100%;
                    height: 100%;
                    position: relative;
                    overflow: hidden;
                    padding: 20px;
                    border-radius: 5px;
                    border: 1px solid #E1E1E1;
                    cursor: pointer;
                    transition: .5s;
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    &:hover {
                        box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.336);
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
                    .best__image {
                        position: relative;
                        margin-bottom: 17px;
                        span {
                            position: absolute;
                            top: 0;
                            right: 0;
                            color: var(--link);
                            &:hover {
                                color: #F74B81;
                            }
                        }
                    }
                    .best__slide-footer {
                        display: flex;
                        flex-direction: column;
                        align-items: flex-start;
                        & > p {
                            font-size: 13px;
                            color: var(--link);
                            font-weight: 500;
                            margin-bottom: 3px;
                        }
                        h4 {
                            font-size: 20px;
                            letter-spacing: 0.005em;
                            color: var(--text);
                            margin-bottom: 5px;
                        }
                        .best__slide-stars {
                            color: var(--star);
                            font-size: 25px;
                            display: flex;
                            column-gap: 3px;
                            margin-bottom: 10px;
                        }
                        .best__slide-price {
                            div {
                                text-align: left;
                                & > p {
                                    font-size: 12px;
                                    font-weight: 500;
                                    color: var(--link);
                                }
                                .price {
                                    font-size: 16px;
                                    color: var(--text);
                                    font-weight: 700;
                                    margin: 10px 0;
                                    span:nth-of-type(2) {
                                        font-size: 14px;
                                        color: var(--link);
                                        font-weight: 400;
                                        margin-left: 5px;
                                    }
                                }
                            }
                        }
                        button {
                            background: var(--btn);
                            padding: 10px 0;
                            width: 100%;
                            border-radius: 5px;
                            width: 100%;
                            font-size: 14px;
                            color: var(--white);
                            text-transform: capitalize;
                            display: flex;
                            justify-content: center;
                            column-gap: 10px;
                            transition: .5s;
                            &:hover {
                                box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.336);
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>