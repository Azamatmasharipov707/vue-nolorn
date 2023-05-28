<template>
    <section class="nextpage">
        <div class="container">
            <NavbarTop />
            <Navbar />

            <div class="topnext">
                <div class="next__nav">
                    <h2>Rice drink with vitamin D3 </h2>
                    <p>Art.No. 183260098 </p>
                </div>
                <ul class="next__list">
                    <li class="next__item"><a href="#!" class="next__link">General info</a></li>
                    <li class="next__item"><a href="#!" class="next__link">Product details</a></li>
                    <li class="next__item"><a href="#!" class="next__link">Reviews</a></li>
                </ul>
            </div>


            <div class="main__next">
                <img src="" alt="">
                <div class="main__info">
                    <div class="info__top">
                        <div>

                            <p class="price">
                                <span>$ 15.50 </span>
                                <del>$31.00</del>
                                <span class="discount"></span>
                            </p>
                            <div class="main__next-stars">
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                            <button><font-awesome-icon style="color: var(--text);" :icon="['fas', 'star']" /></button>

                        </div>
                        </div>
                    </div>
                </div>
            </div>


        </div>
    </section>
</template>

<script setup>
import NavbarTop from '../components/NavbarTop.vue';
import Navbar from '../components/Navbar.vue';

</script>

<style lang="scss" scoped>
.nextpage {
    border-top: 10px solid;
    margin: 200px 0;

    .container {
        .topnext {
            padding: 20px 0;

            border-bottom: 1px solid var(--border);

            .next__nav {

                display: flex;
                align-items: center;
                justify-content: space-between;
                margin-bottom: 20px;

                h2 {
                    font-size: 48px;
                    font-weight: 500;
                    line-height: 56px;
                    font-family: var(--f-Uniform);
                    color: var(--black);

                }

                p {
                    font-weight: 500;
                    font-size: 16px;
                    line-height: 19px;
                    color: #4D606E;
                }

            }

            .next__list {
                display: flex;
                align-items: center;
                padding: 20px 0;


                .next__item {
                    .next__link {

                        transition: .5s;
                        padding: 16px 37px;
                        color: var(--text);

                        &:hover {
                            border: 1px solid var(--border);
                            color: var(--link-hover);

                        }
                    }


                }
            }
        }

    }
}</style>