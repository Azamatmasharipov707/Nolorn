<script setup>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

import { ref } from 'vue';

const shopObj = ref([
    {
        image: '../public/image/categories/sets.svg',
        name: 'Sets',
        bgColor: '#D4EEE2'
    },
    {
        image: '../public/image/categories/fruits.svg',
        name: 'Fruits',
        bgColor: '#F4EAEA'
    },
    {
        image: '../public/image/categories/Vejetables.svg',
        name: 'Vejetables',
        bgColor: '#D9F2F9'
    },
    {
        image: '../public/image/categories/Greenery.svg',
        name: 'Greenery',
        bgColor: '#F2EBD9'
    },
    {
        image: '../public/image/categories/Fungi.svg',
        name: 'Fungi',
        bgColor: '#D4EEE2'
    },
    {
        image: '../public/image/categories/Groceries.svg',
        name: 'Groceries',
        bgColor: '#D9F2F9'
    },
    {
        image: '../public/image/categories/Sweets.svg',
        name: 'Sweets',
        bgColor: '#D4EEE2'
    },
    {
        image: '../public/image/categories/Drinks.svg',
        name: 'Drinks',
        bgColor: '#D9F2F9'
    },
    {
        image: '../public/image/categories/Groceries.svg',
        name: 'Groceries',
        bgColor: '#D4EEE2'
    },
    {
        image: '../public/image/categories/fruits.svg',
        name: 'Fruits',
        bgColor: '#fff'
    },
    {
        image: '../public/image/categories/sets.svg',
        name: 'Sets',
        bgColor: '#D4EEE2'
    },
    {
        image: '../public/image/categories/Groceries.svg',
        name: 'Groceries',
        bgColor: '#D4EEE2'
    },
])


</script>

<template>
    <div class="cotegories">
        <div class="container">
            <div class="cotegories__top">
                <h2 class="title">Shop <span class="title-span">by Categories</span></h2>
            </div>
            <carousel :items-to-show="8" class="cotegories__cards">
                <Slide v-for="slide in shopObj" :key="slide" :style="{background: slide.bgColor}" class="cotegories__card">
                    <img :src="slide.image" alt="">
                    <p>{{ slide.name }}</p>
                </Slide>
                <template #addons>
                    <Navigation  />
                </template>
            </carousel>
        </div>
    </div>
</template>
  


<style lang="scss" scoped>
.cotegories {
    padding: 40px 0 80px;

    .container {
        position: relative;
        
        .cotegories__cards {
            .cotegories__card {
                max-width: 120px;
                min-height: 120px;
                border-radius: 5px;
                border: 1px solid #E4E5E9;
                // background: red;
                margin: 0 15px;
                display: flex;
                flex-direction: column;
                transition: 500ms;
                cursor: pointer;
                &:hover {
                    box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.1);
                }
                p {
                    font-size: 12px;
                    color: var(--text);
                    margin-top: 10px;
                }
            }
            .carousel__prev {
                width: 50px;
                background: red !important;
            }
        }
    
    }
}
</style>