<template>
    <section class="fruits">
        <div class="container">
            <div class="fruits__card" v-for="fruit in fruits2Obj">
                <div class="fruits__content">
                    <h2>{{ fruit.title }}</h2>
                    <Button />
                </div>
                <img :src="fruit.image" alt="" class="fruits__img">
            </div>

        </div>
    </section>
</template>

<script setup>
import Button from './Button.vue'
import { reactive } from 'vue';


const fruits2Obj = reactive([
    {
        image: '../src/image/fruits/pngwing 4.svg',
        title: 'Vegetarian and Vegan products',
    },
    {
        image: '../src/image/fruits/pngwing 5.svg',
        title: 'Vegetarian and Vegan products',
    },
    {
        image: '../src/image/fruits/pngwing 6.svg',
        title: 'Vegetarian and Vegan products',
    }

])
</script>

<style lang="scss" scoped>
.fruits {
    margin: 80px 0; 
    .container {
        display: flex;
        // column-gap: 30px;
        justify-content: space-between;

        .fruits__card {
            min-height: 210px;
            max-width: 370px;
            width: 100%;
            border: 1px solid var(--border);
            border-radius: 5px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            transition: .5s;
            position: relative;

            &:hover {
                box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.572);
            }

            .fruits__content {

                h2 {
                    font-size: 20px;
                    color: var(--title);
                    margin-bottom: 6px;
                    max-width: 231px;
                    width: 100%;
                }

            }
            .fruits__image{
                position: absolute;
                z-index: -1;

            }


        }
    }
}
</style>