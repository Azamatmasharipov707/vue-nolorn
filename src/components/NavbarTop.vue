<template>
    <div class="navbar-top">
        <div class="container">
            <a href="#!" class="navbar-top__logo"><img src="../image/logo.svg" alt=""></a>
            <div class="navbar-top__input">
                <select name="" id="">
                    <option value="">All cotegories</option>
                    <option value="">All cotegories</option>
                    <option value="">All cotegories</option>
                </select>
                <div>
                    <input type="search" placeholder="Search...">
                    <font-awesome-icon class="navbar-top__search" :icon="['fasr', 'magnifying-glass']" />
                </div>
            </div>
            <div class="navbar-top__right">
                <div class="navbar-top__selects">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
                    </svg>
                    <select name="" id="">
                        <option value="">All cotegories</option>
                        <option value="">All cotegories</option>
                        <option value="">All cotegories</option>
                        <option value="">All cotegories</option>
                    </select>
                </div>
                <div class="navbar-top__shop">
                    <button>
                        <div>
                            <span>1</span>
                            <font-awesome-icon class="navbar-top__shop-icon" :icon="['fasl', 'heart']" />
                        </div>
                        Wishlist
                    </button>
                    <button>
                        <div>
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                            </svg>
                            <span>1</span>
                        </div>
                        Card
                    </button>
                    <button>
                        <font-awesome-icon class="navbar-top__shop-icon" :icon="['far', 'user']" />
                        Account
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.navbar-top {
    padding: 30px 0;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .navbar-top__input {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 20px;
            border: 1px solid var(--border);
            border-radius: 5px;
            max-width: 466px;
            width: 100%;
            select {
                border: none;
                outline: none;
                font-family: var(--f_Uniform);
                font-weight: 500;
                font-size: 14px;
                line-height: 15px;
                cursor: pointer;
                padding-right: 10px;
                border-right: 1.5px solid var(--border);
                margin-right: 8px;
            }
            div {
                display: flex;
                width: 100%;
                input {
                    width: 100%;
                    &::placeholder {
                        font-family: var(--f_Uniform);
                        font-weight: 500;
                    }
                }
                .navbar-top__search {
                    font-size: 18px;
                    color: var(--icon-1);
                }
            }
        }
        .navbar-top__right {
            display: flex;
            justify-content: space-between;
            align-items: center;
            column-gap: 20px;
            .navbar-top__selects {
                display: flex;
                column-gap: 8px;
                padding: 10px;
                border-radius: 5px;
                &:hover {
                    box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.326);
                }
                select {
                    color: var(--link-hover);
                }
                svg {
                    width: 27px;
                    color: var(--icon-1);
                }
            }
            .navbar-top__shop {
                display: flex;
                column-gap: 10px;
                button {
                    display: flex;
                    align-items: center;
                    column-gap: 5px;
                    font-size: 14px;
                    color: var(--title);
                    padding: 5px 7px;
                    border-radius: 5px;
                    &:hover {
                        box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.326);
                    }
                    div {
                        position: relative;
                        span {
                            width: 14px;
                            height: 14px;
                            background: var(--link-hover);
                            position: absolute;
                            top: -6px;
                            right: -6px;
                            border-radius: 50%;
                            font-size: 12px;
                            color: var(--white);
                        }
                    }
                    .navbar-top__shop-icon {
                        font-size: 16px;
                    }
                    svg {
                        width: 20px;
                    }
                }
            }
        }
    }
}
</style>