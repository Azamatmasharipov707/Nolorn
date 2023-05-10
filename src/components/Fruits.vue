<template>
  <div class="fruits">
    <div class="container">
      <div class="fruits__card" v-for="fruit in fruits" :style="{background: fruit.bgColor}">
        <img :src="fruit.image" alt="" class="fruits__img">
        <div class="fruits__content">
            <h3>{{ fruit.title }}</h3>
            <Button />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'
import Button from './Button.vue'

const fruits = reactive([
    { image: '../public/image/categories/orange.png', bgColor: '#F2EBD9', title: 'Vegetarian and vegan products' },
    { image: '../public/image/categories/pngwing.png', bgColor: '#F4EAEA', title: 'Vegetarian and vegan products' },
    { image: '../public/image/categories/klupnika.png', bgColor: '#E9ECF4', title: 'Vegetarian and vegan products' },
])
</script>

<style lang="scss" scoped>
.fruits {
    margin-bottom: 80px;
    .container {
        display: flex;
        justify-content: space-between;
        .fruits__card {
            max-width: 370px;
            width: 100%;
            min-height: 230px;
            border-radius: 10px;
            position: relative;
            display: flex;
            padding: 30px 22px;
            .fruits__img {
                position: absolute;
                right: 0;
                bottom: 13px;
            }
            .fruits__content {
                position: relative;
                flex-grow: 1;
                display: flex;
                flex-direction: column;
                justify-content: flex-end;
                h3 {
                    font-size: 22px;
                    font-weight: 500;
                    margin-bottom: 10px;
                    color: var(--text);
                }
            }
        }
    }
}
</style>
