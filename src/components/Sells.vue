<template>
    <section class="sells">
        <div class="container">
            <h2 class="sells__title title">Daily<span class="title-span">Best Sells</span></h2>
            <carousel :items-to-show="4" class="sells__slider">
                <slide class="sells__slide">
                    <div class="sells__card sells__slide-first">
                        <h2>A Burst of energy</h2>
                        <Button />
                    </div>
                </slide>
                <slide class="sells__slide" v-for="sells in sellsObj">
                    <div class="sells__card">
                        <div class="hot" :class="sells.line == 'hot' ? 'active' : ''">
                            <p>hot</p> 
                        </div>
                        <div class="hot2" :class="sells.line == 'hot2' ? 'active' : ''">
                            <p>hot</p> 
                        </div>
                        <div class="sells__image">
                            <span>
                                <font-awesome-icon :icon="['fas', 'heart']" />
                            </span>
                            <img :src="sells.image" alt="">
                        </div>
                        <div class="sells__footer">
                            <p>Category</p>
                            <h4>{{ sells.title }}</h4>
                            <div class="sells__card-stars">
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon style="color: var(--text);" :icon="['fas', 'star']" /></button>
                            </div>
                            <div class="sells__card-price">
                                <div>
                                    <p>Piker per kg</p>
                                    <p class="price">
                                        <span>{{ sells.price }}</span>
                                        <del>{{ sells.previos }}</del>
                                    </p>
                                </div>
                                <button>
                                    <font-awesome-icon class="add-btn" :icon="['fas', 'cart-shopping']" />
                                    <span>Add to Cart</span>
                                </button>
                            </div>
                        </div>
                    </div>
                </slide>
                
                <template #addons>
                    <navigation />
                    <pagination />
                </template>
            </carousel>
        </div>
        </section>
  </template>
  
  <script setup>
  // If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
  import 'vue3-carousel/dist/carousel.css'
  import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
  import Button from './Button.vue'
  import { reactive } from 'vue';

  const sellsObj = reactive([
    {
        image: '../src/image/Sells/pngwing 13.png',
        title: 'Gorih pecan',
        price: '$24.00',
        previos: '$30.00',
        line: 'hot2'
    },
    {
        image: '../src/image/Sells/pngwing 14.png',
        title: 'Gorih pecan',
        price: '$24.00',
        previos: '$30.00',
        line: 'hot'
    },
    {
        image: '../src/image/Sells/pngwing 15.png',
        title: 'Gorih pecan',
        price: '$24.00',
        previos: '$30.00',
        line: 'hot2'
    },
    {
        image: '../src/image/Sells/pngwing 13.png',
        title: 'Gorih pecan',
        price: '$24.00',
        previos: '$30.00',
        line: 'hot'
    },
    {
        image: '../src/image/Sells/pngwing 15.png',
        title: 'Gorih pecan',
        price: '$24.00',
        previos: '$30.00',
        line: 'hot2'
    },
  ])

 /*  export default {
    name: 'App',
    components: {
      Carousel,
      Slide,
      Pagination,
      Navigation,
    },
  } */
  </script>

<style lang="scss" scoped>
.sells {
    .container {
        .sells__slider {
            margin: 30px 0 80px;
            .sells__slide {
                text-align: left;
                .sells__slide-first {
                   height: 100%;
                   background: url(../image/Sells/cofe.png);
                   display: flex;
                   flex-direction: column;
                   justify-content: flex-end;
                   h2 {
                    font-size: 40px;
                    line-height: 48px;
                    margin-bottom: 30px;
                    color: var(--white);
                   }
                }
                .sells__card {
                    border: 1px solid var(--border);
                    border-radius: 5px;
                    max-width: 270px;
                    width: 100%;
                    height: 100%;
                    padding: 20px;
                    position: relative;
                    overflow: hidden;
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    .hot, .hot2 {
                        position: absolute;
                        background: #67BCEE;
                        color: var(--white);
                        width: 128px;
                        padding: 10px 0;
                        text-align: center;
                        text-transform: capitalize;
                        transform: rotate(-45deg);
                        top: 10px;
                        left: -33px;
                        display: none;
                    &.active {
                        display: block;
                    }
                }
                .hot2 {
                    background: #F74B81;
                }
                    .sells__image {
                        position: relative;
                        margin-top: 20px;
                        span {
                            position: absolute;
                            top: 0;
                            right: 0;
                            &:hover {
                                color: #F74B81;
                            }
                        }
                    }
                    .sells__footer {
                        p {
                            font-size: 14px;
                            color: var(--text);
                            font-weight: 500;
                        }
                        h4 {
                            font-size: 20px;
                            color: var(--title);
                            margin: 5px 0;
                        }
                        .sells__card-stars {
                            display: flex;
                            column-gap: 3px;
                            button {
                                color: var(--star);
                                font-size: 18px;
                            }
                        }
                        .sells__card-price {
                            div {
                                .price {
                                    margin: 8px 0;
                                    font-weight: 700;
                                    color: var(--title);
                                    font-size: 16px;
                                    del {
                                        color: var(--text);
                                        font-size: 13px;
                                    }
                                }
                            }
                            button {
                                width: 100%;
                                background: var(--btn);
                                border-radius: 5px;
                                padding: 10px 0;
                                color: var(--white);
                                font-size: 16px;
                                display: flex;
                                justify-content: center;
                                column-gap: 10px;
                                transition: .5s;
                                &:hover {
                                    box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.272);
                                }
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>
  
