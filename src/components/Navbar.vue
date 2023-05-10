<template>
    <nav class="nav">
        <div class="container">
            <button class="nav__btn btn">
                <img src="../image/nav/menu.svg" alt="">
                <select name="" id="">
                    <option value="">Browse All Categories</option>
                    <option value="">About</option>
                    <option value="">Shop</option>
                    <option value="">Blog</option>
                </select>
            </button>
            <ul class="nav__list">
                <li class="nav__item" v-for="link in links">
                    <a href="#!" class="nav__link">
                        {{ link }}
                        <font-awesome-icon :icon="['fas', 'angle-down']" />
                    </a>
                </li>
                <li class="nav__item socials">
                    <a href="#!" class="nav__link"><font-awesome-icon :icon="['fab', 'facebook']" /></a>
                    <a href="#!" class="nav__link"><font-awesome-icon :icon="['fab', 'twitter']" /></a>
                    <a href="#!" class="nav__link"><font-awesome-icon :icon="['fab', 'instagram']" /></a>
                    <a href="#!" class="nav__link"><font-awesome-icon :icon="['fab', 'youtube']" /></a>
                    <a href="#!" class="nav__link"><font-awesome-icon :icon="['fab', 'whatsapp']" /></a>
                </li>
            </ul>
            <div class="nav__call">
                <a href="#!">
                    <font-awesome-icon class="nav__call-icon" :icon="['fas', 'phone-volume']" />
                    <p>
                        (406) 555-0120
                        <span>Men-F+9 00-20 00</span>
                    </p>
                </a>
            </div>
        </div>
    </nav>
</template>

<script setup>
import { reactive } from 'vue';


const links = reactive(['Home', 'About', 'Shop', 'Blog', 'Our team', 'Contact',]);

</script>

<style lang="scss" scoped>
.nav {
    border-top: 1px solid rgba(0, 0, 0, 0.2);
    border-bottom: 1px solid rgba(0, 0, 0, 0.2);
    padding: 10px 0;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
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
        .nav__list {
            display: flex;
            align-items: center;
            column-gap: 25px;
            .nav__item {
                
                .nav__link {
                    display: flex;
                    align-items: center;
                    font-size: 14px;
                    color: var(--link);
                    line-height: 15px;
                    column-gap: 10px;
                    transition: .5s;
                    font-weight: 500;
                    &:hover {
                        color: var(--link-hover);
                    }
                }
            }
            .socials {
                display: flex;
                column-gap: 10px;
                .nav__link {
                    font-size: 18px;
                    color: var(--icon-2);
                    transition: .5s;
                    &:hover {
                        transform: rotate(360deg);
                    }
                }
            }
        }
        .nav__call {
            border-left: 2px solid var(--icon-1);
            padding-left: 24px;
            a {
                display: flex;
                align-items: center;
                column-gap: 7px;
                color: var(--icon-2);
                font-size: 19px;
                .nav__call-icon {
                    transition: .5s;
                }
                &:hover {
                    .nav__call-icon {
                        color: var(--link-hover);
                    }
                }
                p {
                    font-size: 17px;
                    span {
                        display: block;
                        font-size: 10px;
                        color: var(--icon-1);
                    }
                }
            }
        }
    }
}
</style>