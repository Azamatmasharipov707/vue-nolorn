<template>
    <section>
        <div class="container">
            <div class="product__nav">
                <h2 class="title">Popular <span class="title-span">Products</span></h2>
                <ul class="product__list">
                    <li>
                        <button @click="tabIndex = 1" :class="tabIndex == 1 ? 'active' : ''">All</button>
                    </li>
                    <li>
                        <button @click="tabIndex = 2" :class="tabIndex == 2 ? 'active' : ''">Milks</button>
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
            <div class="product__cards" v-if="tabIndex == 1">
                <div class="product__card" v-for="card in cardObj" :key="card">
                    <div class="hot" :class="card.line == 'hot' ? 'active': '' ">
                        <p>hot</p> 
                    </div>
                    <div class="hot2" :class="card.line == 'hot2' ? 'active': ''">
                        <p>hot</p> 
                    </div>
                    <div class="product__image">
                        <span>
                            <font-awesome-icon :icon="['fas', 'heart']" />
                        </span>
                        <img :src="card.image" alt="">
                    </div>
                    <div class="product__footer">
                        <p>Category</p>
                        <h4>{{ card.title }}</h4>
                        <div class="product__card-stars">
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon style="color: var(--text);" :icon="['fas', 'star']" /></button>
                        </div>
                        <div class="product__card-price">
                            <div>
                                <p>Piker per kg</p>
                                <p class="price">
                                    <span>{{ card.price }}</span>
                                    <del>{{ card.previos }}</del>
                                </p>
                            </div>
                            <button>
                                <font-awesome-icon class="add-btn" :icon="['fas', 'cart-shopping']" />
                                <span>Add</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="product__cards" v-if="tabIndex == 2">
                <div class="product__card" v-for="card in cardObj2" :key="card">
                    <div class="hot" :class="card.line == 'hot' ? 'active': '' ">
                        <p>hot</p> 
                    </div>
                    <div class="hot2" :class="card.line == 'hot2' ? 'active': ''">
                        <p>hot</p> 
                    </div>
                    <div class="product__image">
                        <span>
                            <font-awesome-icon :icon="['fas', 'heart']" />
                        </span>
                        <img :src="card.image" alt="">
                    </div>
                    <div class="product__footer">
                        <p>Category</p>
                        <h4>{{ card.title }}</h4>
                        <div class="product__card-stars">
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon style="color: var(--text);" :icon="['fas', 'star']" /></button>
                        </div>
                        <div class="product__card-price">
                            <div>
                                <p>Piker per kg</p>
                                <p class="price">
                                    <span>{{ card.price }}</span>
                                    <del>{{ card.previos }}</del>
                                </p>
                            </div>
                            <button>
                                <font-awesome-icon class="add-btn" :icon="['fas', 'cart-shopping']" />
                                <span>Add</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
section {
    margin-bottom: 80px;
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
                        font-size: 20px;
                        font-weight: 500;
                        color: var(--text);
                        &.active {
                            color: var(--link-hover);
                        }
                    }
                }
            }
        }
        .product__cards {

            display: flex;
            flex-wrap: wrap;
            gap: 21px;
            margin-top: 40px;
            .product__card {
                
                border: 1px solid var(--border);
                border-radius: 10px;
                max-width: 269px;
                width: 100%;
                padding: 23px;
                position: relative;
                overflow: hidden;
                transition: .5s;
                /* display: flex;
                flex-direction: column;
                justify-content: space-between; */
                &:hover {
                    box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.274);
                }
                .hot, .hot2 {
                    position: absolute;
                    background: #67BCEE;
                    color: var(--white);
                    width: 128px;
                    padding: 10px 0;
                    text-align: center;
                    text-transform: capitalize;
                    transform: rotate(-45deg);
                    top: 10px;
                    left: -33px;
                    display: none;
                    &.active {
                        display: block;
                    }
                }
                .hot2 {
                    background: #F74B81;
                }
                .product__image {
                    position: relative;
                    width: 100%;
                    height: 210px;
                    img {
                        width: 100%;
                        height: 100%;
                        // object-fit: cover;
                    }
                    span {
                        position: absolute;
                        right: 0;
                        &:hover {
                            color: #F74B81;
                            cursor: pointer;
                        }
                    }
                }
                .product__footer {
                    margin-top: 40px;
                    p {
                        font-size: 13px;
                        font-weight: 500;
                        color: var(--text);
                    }
                    h4 {
                        font-size: 20px;
                        font-weight: 600;
                        color: var(--title);
                        margin: 8px 0;
                    }
                    .product__card-stars {
                        display: flex;
                        column-gap: 4px;
                        margin-bottom: 17px;
                        button {
                            color: var(--star);
                            font-size: 23px;
                        }
                    }
                    .product__card-price {
                        display: flex;
                        align-items: center;
                        justify-content: space-between;
                        div {
                            .price {
                                color: var(--title);
                                font-size: 16px;
                                font-weight: 700;
                                del {
                                    color: var(--text);
                                    font-size: 13px;
                                    font-weight: 500;
                                }
                            }
                        }
                        button {
                            display: flex;
                            align-items: center;
                            column-gap: 20px;
                            border-radius: 5px;
                            background: #D4EEE2;
                            font-size: 13px;
                            font-weight: 500;
                            padding: 10px;
                            color: var(--link-hover);
                            transition: .5s;
                            .add-btn {
                                font-size: 16px;
                            }
                            &:hover {
                                box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.274);
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>

<script setup>
import { reactive, ref } from 'vue';

const tabIndex = ref(1);

const cardObj= reactive([
    {
        image: '../src/image/products/kadi.png',
        title: 'Garbuz Ukraine',
        price: '$26.00',
        previos: '$38.00',
        line: 'hot'
    },
    {
        image: '../src/image/products/priprava.png',
        title: 'Ground allspice ',
        price: '$22.00',
        previos: '$24.00',
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
        price: '$32.00',
        previos: '$45.00',
        line: 'hot2'
    },
    {
        image: '../src/image/products/karam.png',
        title: 'Boston',
        price: '$24.00',
        previos: '$26.00',
        line: 'hot2'
    },
    {
        image: '../src/image/products/pngwing 12.png',
        title: 'Petya Zhovta',
        price: '$28.00',
        previos: '$32.00',
        line: 'hot'
    },
    {
        image: '../src/image/products/lovya.png',
        title: 'Boby Edamame c/m',
        price: '$24.00',
        previos: '$30.00',
    },
    {
        image: '../src/image/products/kiwi.png',
        title: 'Kiwi Gold',
        price: '$21.00',
        previos: '$23.00',
        line: 'hot2'
    },
    {
        image: '../src/image/products/qoziqorin.png',
        title: 'Mushhroom Shiitake',
        price: '$24.00',
        previos: '$30.00',
        line: 'hot'
    }
  
])
const cardObj2= reactive([
    {
        image: '../src/image/products/karam.png',
        title: 'Boston',
        price: '$24.00',
        previos: '$26.00',
        line: 'hot2'
    },
    {
        image: '../src/image/products/priprava.png',
        title: 'Ground allspice ',
        price: '$22.00',
        previos: '$24.00',
    },
    {
        image: '../src/image/products/gashr.png',
        title: 'Wash the carot',
        price: '$32.00',
        previos: '$45.00',
        line: 'hot2'
    },
    {
        image: '../src/image/products/pngwing 12.png',
        title: 'Petya Zhovta',
        price: '$28.00',
        previos: '$32.00',
        line: 'hot'
        
    },
    {
        image: '../src/image/products/kadi.png',
        title: 'Garbuz Ukraine',
        price: '$26.00',
        previos: '$38.00',
        line: 'hot'
    },
    {
        image: '../src/image/products/lovya.png',
        title: 'Boby Edamame c/m',
        price: '$24.00',
        previos: '$30.00',
    },
    {
        image: '../src/image/products/qoziqorin.png',
        title: 'Mushhroom Shiitake',
        price: '$24.00',
        previos: '$30.00',
        line: 'hot'
    },
    {
        image: '../src/image/products/kiwi.png',
        title: 'Kiwi Gold',
        price: '$21.00',
        previos: '$23.00',
        line: 'hot2'
    }
  
])

</script>

