<template>
    <section>
        <div class="container">
            <div class="product__nav">
                <h2 class="title">Popular <span class="title-span">Products</span></h2>
                <ul class="product__list">
                    <li>
                        <button>All</button>
                    </li>
                    <li>
                        <button>Milks</button>
                    </li>
                    <li>
                        <button>Pet Foods</button>
                    </li>
                    <li>
                        <button>Vegetables </button>
                    </li>
                    <li>
                        <button>Fruits</button>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
section {
    .container {
        .product__nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            .product__list {
                display: flex;
                column-gap: 20px;
                li {
                    button {
                        

                    }
                }
            }
        }
    }
}
</style>

<script setup>
import { reactive } from 'vue';

const cardObj= reactive([
    {
        image: '../src/image/products/kadi.png',
        title: 'Garbuz Ukraine',
       
    },
    {
        image: '../src/image/products/priprava.png',
        title: 'Ground allspice ',   
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
       
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
       
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
       
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
       
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
       
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
       
    },
     {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
       
    },


    

])

</script>

