<template>
    <section class="allproducts">
        <div class="container">
            <div class="allproduct__cards"  v-for="index in cardsObj">
                <h2 class="allproducts__title title">{{ index.title }} <span class="title-span">{{ index.span }}</span></h2>
                <div class="allproducts__card"  v-for="item in cardObj">
                    

                        <img :src="item.image" alt="" class="card__img">
                        <div class="card__info">
                            <h4>Product name</h4>
                            <div class="allproducts__card-stars">
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon style="color: var(--text);" :icon="['fas', 'star']" /></button>
                                <span>(4.0)</span>
                            </div>
                            <p>Additional text</p>
                            <p class="price">
                                <span>$24.00</span>
                                <del> $30.00</del>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        
    </section>
</template>

<script setup>
import { reactive } from 'vue';

const cardsObj = reactive([
    {
        title: 'Top',
        span: 'Selling',


    },
    {
        title: 'Trending',
        span: 'Products',

    },
    {
        title: 'Recently',
        span: 'Added',

    },

])

const cardObj = reactive([
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    }
])

</script>

<style lang="scss" scoped>
.allproducts {
    .container {
        display: flex;
        column-gap: 30px;
        .allproduct__cards {
            
            .allproducts__title {
                border-bottom: 1px solid var(--border);
                max-width: 370px;
                width: 100%;
                font-size: 36px;
                line-height: 42px;

            }

            .allproducts__card {
                display: flex;
                margin: 20px 0;
                

                    
                    .card__img {
                        max-width: 167px;
                        width: 100%;
                        background: var(--white);
                        border: 1px solid var(--border);
                        border-radius: 5px;
                        margin-right: 8px;
                    }
                    
                    .card__info {
                        display: flex;
                        flex-direction: column;
                        row-gap: 5px;
                        
                        h4 {
                            font-size: 20px;
                            font-weight: 400;
                            line-height: 24px;
                            color: var(--title);
                        }
                        
                        .allproducts__card-stars {
                            display: flex;
                        column-gap: 3px;
                        margin-bottom: 5px;
                        
                        button {
                            color: var(--star);
                            font-size: 20px;
                        }
                        
                        span {
                            color: var(--title);
                            font-weight: 500;
                        }
                    }
                    
                    p {
                        font-weight: 400;
                        font-size: 14px;
                        line-height: 17px;
                        color: var(--text);
                        
                    }
                    
                    .price {
                        
                        color: var(--title);
                        font-weight: 700;
                        
                        del {
                            font-size: 14px;
                            font-weight: 400;
                            color: var(--text);
                        }
                    }
                    
                }
            }
        }
    }
}
</style>