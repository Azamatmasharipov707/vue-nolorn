<template>
    <section class="sells">
        <div class="container">
            <h2 class="title">Daily <span class="title-span">Best Sells</span> </h2>
            <Carousel :items-to-show="1.5" class="sells__slider">
                <Slide class="sells__slide">
                    <div class="sells__card">
                        <h1>A Burst of energy</h1>
                        <Button />
                    </div>
                </Slide>

                <template #addons>
                    <Navigation />
                    <Pagination />
                </template>
            </Carousel>
        </div>
    </section>
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

<style scoped lang="scss">
.sells {
    .container {
        
    }
}
</style>