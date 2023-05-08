<template>
    <nav class="nav">
        <div class="container">
            <button class="nav__btn btn">
                <img src="../../public/image/nav/menu.svg" alt="">
                <select name="" id="">
                    <option value="">Browse All Categories</option>
                    <option value="">About</option>
                    <option value="">Shop</option>
                    <option value="">Blog</option>
                </select>
            </button>
            <ul class="nav__list">
                <li class="nav__item">
                    <a href="#!" class="nav__link">
                        home
                    </a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.nav {
    .container {
        .nav__btn {
            max-width: 253px;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            column-gap: 10px;
            select {
                color: var(--white);
                padding-right: 10px;
                option {
                    color: var(--link-hover);
                }
            }
        }
    }
}
</style>