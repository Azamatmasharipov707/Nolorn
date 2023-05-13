<template>
    <div class="best">
        <div class="container">
            <h2 class="title">Daily<span class="title-span">Best Sells</span></h2>
            <carousel class="best__slider" :items-to-show="1.5">
                <slide class="best__slide" v-for="slide in 10" :key="slide">
                    
                </slide>

                <template #addons>
                    <navigation />
                    <pagination />
                </template>
            </carousel>
        </div>
    </div>
</template>

<script setup>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
</script>

<style lang="scss" scoped>

</style>