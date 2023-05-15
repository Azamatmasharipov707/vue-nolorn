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
                    <button>All</button>
                </li>
                <li>
                    <button>All</button>
                </li>
                <li>
                    <button>All</button>
                </li>
                <li>
                    <button>All</button>
                </li>
            </ul>
            </div>
            

        </div>
    </section>

</template>

<script setup>

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
    }
}

</style>