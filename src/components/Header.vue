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
                <Button />
            </div>
        </div>
    </header>
</template>

<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
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

<style lang="scss" scoped>
.header {
    background: url(../image/header/header-bg.svg) no-repeat #F1FCFF;
    padding: 30px 0;
    .container {
        display: flex;
        column-gap: 30px;
        .header__carousel {
            max-width: 770px;
            background: #D9F2F9;
            width: 100%;
            padding: 46px 0;
            
            .header__carousel-slide {
                padding: 0 31px;
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
                            &::placeholder {
                                color: #b2b2b2;
                            }
                        }
                        button {
                            width: 106px;
                            flex-shrink: 0;
                        }
                    }
                }
            }
        }
        .header__content {
            display: flex;
            flex-direction: column;
            justify-content: center;
            width: 100%;
            background: url(../image/header/header-2.png) no-repeat right bottom #F2EBD9;
            padding-left: 30px;
            h1 {
                font-family: var(--f_Uniform);
                font-weight: 500;
                font-size: 40px;
                line-height: 47px;
                max-width: 168px;
                width: 100%;
                margin-bottom: 30px;
                span {
                    color: var(--link-hover);
                }
            }
        }
    }
}
</style>