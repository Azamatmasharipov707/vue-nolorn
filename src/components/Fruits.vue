<template>
    <div class="fruits">
        <div class="container">
            <div class="fruits__card" v-for="fruit in fruitsObj" :style="{background: fruit.bgColor}">
                <img v-bind:src="fruit.image" alt="">
                <div class="fruits__content">
                    <h2>{{ fruit.title }}</h2>
                    <Button />
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import Button from '../components/Button.vue';
import { reactive } from 'vue';
const fruitsObj = reactive([
    {image: '../src/image/fruits/pngwing1.svg', title: 'Vegetarian and vegan products', bgColor: '#F2EBD9'},
    {image: '../src/image/fruits/pngwing2.svg', title: 'Vegetarian and vegan products', bgColor: '#F4EAEA'},
    {image: '../src/image/fruits/pngwing3.svg', title: 'Vegetarian and vegan products', bgColor: '#E9ECF4'}
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
            padding: 22px;
            img {
                position: absolute;
                right: 0;
                bottom: 0;
            }
            .fruits__content {
                position: relative;
                flex-grow: 1;
                display: flex;
                flex-direction: column;
                justify-content: flex-end;
                z-index: 1;
                h2 {
                    font-size: 22px;
                    font-weight: 500;
                    color: var(--title);
                    margin-bottom: 10px;
                }
            }
        }
    }
}
</style>