<template>
   <header class="header">
        <div class="container">
            <carousel class="header__carousel" :items-to-show="1">
                <slide class="header__carousel-slide">
                    <div class="header__carousel-content">
                        <h1>Rice drink with vitamin D3</h1>
                        <p>Up to 30% off your first order</p>
                        <div class="header__carousel-input">
                            <input type="text" placeholder="Enter your email address">
                            <button class="btn">Subscribe</button>
                        </div>
                    </div>
                    <div class="header__carousel-img">
                        <img src="../../public/image/header/header-img.png" alt="">
                    </div>
                </slide>
                <slide class="header__carousel-slide">
                    <div class="header__carousel-content">
                        <h1>Rice drink with vitamin D3</h1>
                        <p>Up to 30% off your first order</p>
                        <div class="header__carousel-input">
                            <input type="text" placeholder="Enter your email address">
                            <button class="btn">Subscribe</button>
                        </div>
                    </div>
                    <div class="header__carousel-img">
                        <img src="../../public/image/header/header-img.png" alt="">
                    </div>
                </slide>
                <slide class="header__carousel-slide">
                    <div class="header__carousel-content">
                        <h1>Rice drink with vitamin D3</h1>
                        <p>Up to 30% off your first order</p>
                        <div class="header__carousel-input">
                            <input type="text" placeholder="Enter your email address">
                            <button class="btn">Subscribe</button>
                        </div>
                    </div>
                    <div class="header__carousel-img">
                        <img src="../../public/image/header/header-img.png" alt="">
                    </div>
                </slide>
        
                <template #addons>
                    <pagination  />
                </template>
            </carousel>
            <div class="header__content">
                <h1>
                    Buy with
                    <span>
                        free
                        shipping
                    </span>
                </h1>
                <Button />
            </div>
        </div>
    </header>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation, } from 'vue3-carousel'
import Button from './Button.vue';

export default {
  name: 'App',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
    Button
},
}
</script>
<style scoped lang="scss">
.header {
  padding: 30px 0;
  background: url(../../public/image/header/header-bg.png) #f1fcff;
  .container {
    display: flex;
    column-gap: 30px;
    .header__carousel {
      max-width: 770px;
      width: 100%;
      background: #d9f2f9;
      padding: 46px 0;
      .header__carousel-slide {
        justify-content: space-between;
        padding: 30px;
        .header__carousel-content {
          text-align: left;
          h1 {
            font-family: var(--f_Ubuntu);
            font-size: 55px;
            font-weight: 500;
          }
          p {
            font-size: 20px;
            font-family: var(--f_Ubuntu);
            color: var(--link);
            margin: 30px 0;
          }
          .header__carousel-input {
            max-width: 417px;
            width: 100%;
            display: flex;
            justify-content: space-between;
            input {
              width: 100%;
              padding-left: 10px;
            }
            button {
              width: 106px;
              flex-shrink: 0;
            }
          }
        }
      }
      .dots {
        width: 50px;
        height: 50px;
      }
    }
    .header__content {
      background: url(../../public/image/header/header-img2.png) no-repeat right
        bottom #f2ebd9;
      padding-left: 31px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      width: 100%;
      h1 {
        font-size: 40px;
        max-width: 180px;
        width: 100%;
        margin-bottom: 30px;
        span {
          color: var(--link-hover);
        }
      }
    }
  }
}

.carousel__pagination {
  .carousel__pagination-item {
    .carousel__pagination-button::after {
      width: 40px !important;
      height: 40px !important;
    }
  }
}
</style>
