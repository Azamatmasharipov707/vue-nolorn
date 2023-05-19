<template>

    <section class="sells">
        <div class="container">


            <carousel :items-to-show="4">
                <slide v-for="slide in sellObj" :key="slide">

                    <div class="sells__cards" v-for="sells in sellObj">
                        <div class="sells__card">
                        {{ sells.title }}
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
  
  <script>
  // If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
  import 'vue3-carousel/dist/carousel.css'
  import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
  import { reactive } from 'vue'
  
const sellObj = reactive ([
    {
        image: '../src/image/Sells/pngwing 13.png',
        title: 'Gorih pecan' ,
    },
    {
        image: '../src/image/Sells/pngwing 13.png',
        title: 'Gorih pecan' ,
    },
    {
        image: '../src/image/Sells/pngwing 13.png',
        title: 'Gorih pecan' ,
    }
])

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

</style>
  