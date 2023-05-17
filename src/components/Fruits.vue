<template>

<section>
    <div class="container">
        <div class="fruit__cards">
            <div class="fruit__card"  v-for="fruit in fruitObj" :style="{background: fruit.bgColor}">
                <img :src="fruit.image" alt="">
                <div class="fruits__content">

                    <h2>{{ fruit.title }}</h2>
                    <Button />
                </div>
                </div>
        </div>
    </div>
</section>
</template>

<script setup>
import Button from './Button.vue';
import { reactive } from 'vue';

const fruitObj = reactive([

{
        image: '../src/image/fruits/orange_PNG810 1.png',
        title: 'Vegetarian and vegan products',
        bgColor: '#F2EBD9'
    },
    {
        image: '../src/image/fruits/pngwing 1.png',
        title: 'Vegetarian and vegan products',
        bgColor: '#F4EAEA'
    },
    {
        image: '../src/image/fruits/pngwing 2.png',
        title: 'Vegetarian and vegan products',
        bgColor: '#E9ECF4'
    },
])

</script>

<style lang="scss" scoped>

section{
    margin-bottom: 80px;
    .container{
        .fruit__cards{
            display: flex;
            align-items: center;
            justify-content: space-between;

            .fruit__card{
                max-width: 370px;
                width: 100%;
                min-height: 230px;
                position: relative;
                display: flex;
                border-radius: 10px;
                .fruits__content{
                    flex-grow: 1;
                    display: flex;
                    flex-direction: column;
                    justify-content: flex-end;
                    gap: 10px;
                    z-index: 1;
                    margin: 31px 23px;
                    
                    h2{
                        
                        font-family: var(--f_Inter);
                        font-weight: 500;
                        font-size: 22px;
                        line-height: 27px;
                        color: var(--title);
                        
                        
                    }
                        
                        
                    }

                img{
                    position: absolute;
                    bottom: 0;
                    right: 0;
                    
                }
            }
        }
    }

}



</style>