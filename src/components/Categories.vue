<script setup>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel';
import { reactive } from 'vue';

const shopObj = reactive([
    {
        image: '../src/image/cotegories/Sets.svg',
        title: 'Sets',
        bgColor: '#D4EEE2'
    },
    {
        image: '../src/image/cotegories/fruits.svg',
        title: 'Fruits',
        bgColor: '#fff'
    },
    {
        image: '../src/image/cotegories/Vejetables.svg',
        title: 'Vejetables',
        bgColor: '#F4EAEA'
    },
    {
        image: '../src/image/cotegories/Greenery.svg',
        title: 'Greenery',
        bgColor: '#D9F2F9'
    },
    {
        image: '../src/image/cotegories/Fungi.svg',
        title: 'Fungi',
        bgColor: '#F2EBD9'
    },
    {
        image: '../src/image/cotegories/Groceries.svg',
        title: 'Groceries',
        bgColor: '#D9F2F9'
    },
    {
        image: '../src/image/cotegories/Sweets.svg',
        title: 'Sweets',
        bgColor: '#D9F2F9'
    },
    {
        image: '../src/image/cotegories/Drinks.svg',
        title: 'Drinks',
        bgColor: '#D9F2F9'
    },
    {
        image: '../src/image/cotegories/Drinks.svg',
        title: 'Drinks',
        bgColor: '#F2EBD9'
    },
    {
        image: '../src/image/cotegories/Sweets.svg',
        title: 'Sweets',
        bgColor: '#D9F2F9'
    },
    {
        image: '../src/image/cotegories/Greenery.svg',
        title: 'Greenery',
        bgColor: '#D9F2F9'
    },
    {
        image: '../src/image/cotegories/fruits.svg',
        title: 'Fruits',
        bgColor: '#fff'
    },

])

// //  export default {
//   name: 'App',
//   components: {
//     Carousel,
//     Slide,
//     Pagination,
//     Navigation,
//   },
// } 
</script>

<template>
    <section class="cotegories">
        <div class="container">
            <div class="cotegories__top">
                <h2 class="title">shop <span class="title-span">by Categories</span></h2>
            </div>
            <carousel :items-to-show="1">
                <slide v-for="slide in shopObj" :key="slide">
               
                </slide>

                <template #addons>
                    <navigation />
                </template>
            </carousel>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.cotegories {
    margin: 40px 0 80px;

    .container {
        .cotegories__top {
            margin-bottom: 30px;

        }
            .categories__cards{

                .categories__card{
                    max-width: 120px;
                    width: 100%;
                    min-height: 120px;
                    // background: red;
                    margin: 10px 15px;
                    border-radius: 5px;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    row-gap: 10px;
                    transition: .5s;
                    cursor: pointer;

                    &:hover{
                        box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.545);
                    }

                    p {
                        font-family: var(--f_Uniform);
                        font-size: 14px;
                        letter-spacing: 0.01em;
                        color: var(--text);
                    }
                }
            }
    }
}
</style>
