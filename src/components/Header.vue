<template>
    <header class="header">
        <div class="container">
            <Carousel :items-to-show="1" class="header__carousel">
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
                        <img  src="../image/header/header-1.png" alt="">
                    </div>
                </slide>

                <template #addons>
                    <!-- <navigation /> -->
                    <pagination />
                </template>
            </Carousel>
            <div class="header__content">
                <h1>
                    Buy with
                    <span>free shipping</span>
                </h1>
            </div>
        </div>
    </header>
</template>

<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
    name: 'App',
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
}
</script>

<style lang="scss" scoped>
.header {
    .container {
        display: flex;
        .header__carousel {
            max-width: 770px;
            background: #D9F2F9;
            width: 100%;
            padding: 46px 31px;
            .header__carousel-slide {
                .header__carousel-content {
                    font-family: var(--f_Uniform);
                    text-align: start;
                    h1 {
                        font-size: 55px;
                    }
                    p {
                        font-size: 20px;
                        font-weight: 500;
                        color: var(--icon-1);
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
                    }
                }
            }
        }
    }
}
</style>