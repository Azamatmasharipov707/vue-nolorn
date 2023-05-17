<template>
    <div>
        <NavbarTop />
        <Navbar />
        <Header />
        <Categories />
        <Fruits />
        <Product />
    </div>
</template>

<script setup>
import Categories from '../components/Categories.vue';
import Fruits from '../components/Fruits.vue';
import Header from '../components/Header.vue';
import Navbar from '../components/Navbar.vue';
import NavbarTop from '../components/NavbarTop.vue';
import Product from '../components/Product.vue';
</script>

<style lang="scss" scoped>

</style>