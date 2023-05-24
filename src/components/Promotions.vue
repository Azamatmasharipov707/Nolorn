<template>
    <section class="promotions">
        <div class="container" v-if="sales">
            <h2 class="title">Hot<span class="title-span"> Promotions</span></h2>
            <Carousel :items-to-show="1.5" class="promotions__slider">
                <Slide v-for="item in sales" class="promotions__slide">
                    <div class="promotions__content">
                        <div class="promotions__timer">
                            <div class="promotions__time">
                                <p>Days</p>
                                <span>{{ item.days }}</span>
                            </div>
                            <div class="promotions__time">
                                <p>Hours</p>
                                <span>{{ item.hours % 24 }}</span>
                            </div>
                            <div class="promotions__time">
                                <p>Mins</p>
                                <span>{{ item.minutes % 60 }}</span>
                            </div>
                            <div class="promotions__time">
                                <p>Sec </p>
                                <span>{{ item.seconds % 60 }}</span>
                            </div>
                        </div>
                        <div class="promotions__desc">
                            <h3>Seeds of Change Organic Quinoa,Brown, & Red Rice</h3>
                            <div class="promotions__stars">
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon :icon="['fas', 'star']" />
                                <font-awesome-icon style="color: #939393;" :icon="['fas', 'star']" />
                                <span>(4.0)</span>
                            </div>
                            <p>Additional text</p>
                            <div class="promotions__price">
                                <div>
                                    <p>$24.00</p>
                                    <del>$30.00</del>
                                </div>
                                <button>
                                    <font-awesome-icon :icon="['fas', 'cart-shopping']" />
                                    <span>add</span>
                                </button>
                            </div>
                        </div>
                    </div>
                </Slide>

                <template #addons>
                    <navigation />
                    <pagination />
                </template>
            </Carousel>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'




const sales = ref([])

const launchDate = new Date('1 june 2023')
const launchDate2 = new Date('1 jule 2023')

function timerCount(elem, index) {
    const currDate = new Date();
    const launchTime = elem - currDate;
    let seconds = parseInt(launchTime / 1000)
    let minutes = parseInt(seconds / 60)
    let hours = parseInt(minutes / 60)
    let days = parseInt(hours / 24)
    sales.value[index] = {
        seconds,
        minutes,
        hours,
        days
    }
    return sales.value[index]
}


setInterval(() => {
    timerCount(launchDate, 0)
    timerCount(launchDate2, 1)
}, 1000)


</script>

<style lang="scss" scoped>
.promotions {
    .container {
        .promotions__slider {
            .promotions__slide {
                .promotions__content {
                    background: url(../../public/image/promotions/fruits.png) no-repeat center center / cover;
                    padding: 104px 60px;
                    border-radius: 10px;
                    text-align: left;

                    .promotions__timer {
                        display: flex;
                        justify-content: space-between;
                        margin-bottom: 10px;

                        .promotions__time {
                            background: var(--white);
                            width: 105px;
                            padding: 20px 0;
                            border-radius: 10px;
                            text-align: center;

                            P {
                                font-size: 16px;
                                color: #2FD080;
                                font-weight: 500;
                            }

                            span {
                                font-size: 40px;
                                color: var(--text);
                                font-weight: 500;
                            }
                        }
                    }

                    .promotions__desc {
                        background: var(--white);
                        padding: 20px;
                        border-radius: 10px;
                    }
                }
            }
        }
    }
}
</style>