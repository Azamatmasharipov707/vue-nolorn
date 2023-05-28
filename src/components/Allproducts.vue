<template>
    <section class="allproducts">
        <div class="container">
            <div class="allproduct__cards" >
               <div class="allproducts__titles">
                <h2 class="allproducts__title title"> Top<span class="title-span">Selling</span></h2>
                <h2 class="allproducts__title title"> Trending<span class="title-span">Products</span></h2>
                <h2 class="allproducts__title title"> Recently<span class="title-span">Added</span></h2>
               </div>
                <div class="allproducts__card"  v-for="item in cardObj">
                    

                        <img :src="item.image" alt="" class="card__img">
                        <div class="card__info">
                            <h4>{{ item.namee }}</h4>
                            <div class="allproducts__card-stars">
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                                <button><font-awesome-icon style="color: var(--text);" :icon="['fas', 'star']" /></button>
                                <span>(4.0)</span>
                            </div>
                            <p>{{ item.text }}</p>
                            <p class="price">
                                <span>{{ item.price }}</span>
                                <del> {{ item.previous }}</del>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        
    </section>
</template>

<script setup>
import { reactive } from 'vue';


const cardObj = reactive([
    {
        image:'../src/image/Allproduct/karam.png',
        name:'Product name',
        text:'Additional text',
        price:'$20.00 ',
        previous:'$28.00'
    },
    {
        image:'../src/image/Allproduct/pamidor.png',
        name:'Product name',
        text:'Additional text',
        price:'$22.00 ',
        previous:'$29.00'
    },
    {
        image:'../src/image/Allproduct/shivit.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$30.00'
    },
    {
        image:'../src/image/Allproduct/carrot.png',
        name:'Product name',
        text:'Additional text',
        price:'$26.00 ',
        previous:'$33.00'
    },
    {
        image:'../src/image/Allproduct/yaproq.png',
        name:'Product name',
        text:'Additional text',
        price:'$23.00 ',
        previous:'$27.00'
    },
    {
        image:'../src/image/Allproduct/potato.png',
        name:'Product name',
        text:'Additional text',
        price:'$21.00 ',
        previous:'$27.00'
    },
    {
        image:'../src/image/Allproduct/Kok piyoz.png',
        name:'Product name',
        text:'Additional text',
        price:'$23.00 ',
        previous:'$29.00'
    },
    {
        image:'../src/image/Allproduct/Kok piyoz.png',
        name:'Product name',
        text:'Additional text',
        price:'$24.00 ',
        previous:'$26.00'
    },
    {
        image:'../src/image/Allproduct/Piyoz.png',
        name:'Product name',
        text:'Additional text',
        price:'$25.00 ',
        previous:'$26.00'
    }
])

</script>

<style lang="scss" scoped>
.allproducts {
    .container {
        margin-bottom: 80px;
        .allproduct__cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            .allproducts__titles{
                display: flex;
                column-gap: 30px;
                
                
                
                
                .allproducts__title {
                    border-bottom: 1px solid var(--border);
                    width: 365px;
                    font-size: 36px;
                    line-height: 42px;
                    display: flex;
                    gap: 20px;
                }

            }

            
            

            .allproducts__card {
                display: flex;
                justify-content: space-between;
                max-width: 365px;
                width: 100%;
                margin: 20px 0;
                width: 100%;
                
                

                    
                    .card__img {
                        min-height: 150px;
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