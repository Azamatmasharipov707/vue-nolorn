<script setup>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel';
import { reactive } from 'vue';

const shopObj = reactive([
    {
        image: '../image/cotegories/Sets.svg',
        title: 'Sets',
        bgColor: '#D4EEE2'
    },
    {
        image: '../image/cotegories/fruits.svg',
        title: 'Fruits',
        bgColor: '#fff'
    },
    {
        image: '../image/cotegories/Vejetables.svg',
        title: 'Vejetables',
        bgColor: '#F4EAEA'
    },
    {
        image: '../image/cotegories/Greenery.svg',
        title: 'Greenery',
        bgColor: '#D9F2F9'
    },
    {
        image: '../image/cotegories/Fungi.svg',
        title: 'Fungi',
        bgColor: '#F2EBD9'
    },
    {
        image: '../image/cotegories/Groceries.svg',
        title: 'Groceries',
        bgColor: '#D9F2F9'
    },
    {
        image: '../image/cotegories/Sweets.svg',
        title: 'Sweets',
        bgColor: '#D9F2F9'
    },
    {
        image: '../image/cotegories/Drinks.svg',
        title: 'Drinks',
        bgColor: '#D9F2F9'
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
            <carousel :items-to-show="1.5">
                <slide v-for="shopObj in 10" :key="shopObj">
                    {{shopObj}}
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
        .cotegories__top {}
    }
}
</style>