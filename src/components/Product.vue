<template>

    <section >
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

            <div class="product__cards">
                <div class="product__card">
                    <img src="../image/products/pngwing 4.png" alt="">
                    <div class="product__card-info">
                        <span>Category</span>
                        <h2>Garbuz Ukraine</h2>
                        <ul>
                            <li>
                                <button>

                                    <font-awesome-icon :icon="['fas', 'star']" />
                                </button>
                                </li>
                                <li>
                                <button>

                                    <font-awesome-icon :icon="['fas', 'star']" />
                                </button>
                                </li>
                                <li>
                                <button>

                                    <font-awesome-icon :icon="['fas', 'star']" />
                                </button>
                                </li>
                                <li>
                                <button>

                                    <font-awesome-icon :icon="['fas', 'star']" />
                                </button>
                                </li>
                                <li>
                                <button>

                                    <font-awesome-icon :icon="['fas', 'star']" />
                                </button>
                                </li>
                        </ul>
                        <div class="product__card-price">
                           
                            <p class="card__price">Piker per kg  
                            </p>
                            <span>$24.00 $30.00</span>
                            <button> <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                            </svg> Add</button>
                        </div>
                    </div>
                </div>
            </div>
            

        </div>
    </section>

</template>

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

<style lang="scss" scoped>

section{

    .container{

        .product__nav{
            display: flex;
            justify-content: space-between;
            align-items: center;
            .product__list{
                display: flex;
            }
        }

        .product__card{
            max-width: 269px;
            width: 100%;
            height: 441px;
            border: 1px solid var(--border);
            border-radius: 10px;
            padding: 23px 31px;
            
            img{
                width: 100%;
                margin-bottom: 42px;

            }

            span{
                font-family: var(--f_Inter);
                font-size: 13px;
                line-height: 16px;
                font-weight: 500;
                color: var(--text);
            }

            h2{
                font-family: var(--f_Inter);
                font-size: 20px;
                line-height: 24px;
                font-weight: 600;
                color: var(--title);
                margin: 10px 0;

            }

            ul{
                display: flex;
                column-gap: 3px;
            }

            .product__card-price{
                display: flex;

            }



        }
    }
}

</style>