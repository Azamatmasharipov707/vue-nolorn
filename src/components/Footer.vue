<template>
    <footer class="footer">
        <div class="container">
            <div class="footer__top">
                <ul class="footer__list-first">
                    <li>
                        <h2>
                            <a href="#!" class="title">Nolorn</a>
                        </h2>
                    </li>
                    <li>
                        <div class="socials">
                            <a href="#!" class="footer__link-social"><font-awesome-icon :icon="['fab', 'facebook']" /></a>
                            <a href="#!" class="footer__link-social"><font-awesome-icon :icon="['fab', 'twitter']" /></a>
                            <a href="#!" class="footer__link-social"><font-awesome-icon :icon="['fab', 'instagram']" /></a>
                            <a href="#!" class="footer__link-social"><font-awesome-icon :icon="['fab', 'youtube']" /></a>
                            <a href="#!" class="footer__link-social"><font-awesome-icon :icon="['fab', 'whatsapp']" /></a>
                        </div>
                    </li>
                    <li>
                        <font-awesome-icon class="footer__link-icon" :icon="['fas', 'phone-volume']" />
                        <a href="#!" class="footer__link">(406) 555-0120</a>
                    </li>
                    <li>
                        <font-awesome-icon class="footer__link-icon" :icon="['far', 'envelope']" />
                        <a href="#!" class="footer__link">name@email.com</a>
                    </li>
                    <li>
                        <font-awesome-icon class="footer__link-icon" :icon="['fas', 'location-dot']" />
                        <a href="#!" class="footer__link">6391 Elgin St. Celina, Delawere 10299</a>
                    </li>
                    <li>
                        <font-awesome-icon class="footer__link-icon" :icon="['far', 'clock']" />
                        <a href="#!" class="footer__link">6391 Elgin St. Celina, Delawere 10299</a>
                    </li>
                </ul>
                <ul class="footer__list-second">
                    <li>
                        <h2><a href="#!" class="title">Company</a></h2>
                    </li>
                    <li><a href="#!" class="footer__list-second-link">About Us</a></li>
                    <li><a href="#!" class="footer__list-second-link">Service</a></li>
                    <li><a href="#!" class="footer__list-second-link">Case Studies</a></li>
                    <li><a href="#!" class="footer__list-second-link">Blog</a></li>
                    <li><a href="#!" class="footer__list-second-link">Contact</a></li>
                </ul>
                <ul class="footer__list-third">
                    <li>
                        <h2><a href="#!" class="title">Account</a></h2>
                    </li>
                    <li><a href="#!" class="footer__list-third-link">Sign in</a></li>
                    <li><a href="#!" class="footer__list-third-link">View Cart</a></li>
                    <li><a href="#!" class="footer__list-third-link">My Wishlist</a></li>
                    <li><a href="#!" class="footer__list-third-link">Track My Order</a></li>
                    <li><a href="#!" class="footer__list-third-link">Compare ptoducts</a></li>
                </ul>
                <ul class="footer__list-fourth">
                    <li>
                        <h2><a href="#!" class="title">Download</a></h2>
                    </li>
                    <span>From App Store or Google Play</span>
                    <li>
                        <div class="footer__app-link">
                            <font-awesome-icon class="footer__app-icon" :icon="['fab', 'google-play']" />
                            <div class="google__play-info footer__app-info">
                                <span>Get it on</span>
                                <h2>Google Play</h2>
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="footer__app-link">
                            <font-awesome-icon class="footer__app-icon" :icon="['fab', 'apple']" />
                            <div class="appstore-info footer__app-info">
                                <span>Download on the</span>
                                <h2>App Store</h2>
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="footer__bottom">
                <ul>
                    <li><a href="#!">Copyright © 2023 <span>ThemeRage</span>. All Right Reserved</a></li>
                    <li>
                        <font-awesome-icon class="footer__bottom-icon" :icon="['fas', 'phone-volume']" />
                        <a href="#!">(406) 555-0120</a>
                    </li>
                    <li>
                        <font-awesome-icon class="footer__bottom-icon" :icon="['fas', 'phone-volume']" />
                        <a href="#!">(406) 555-0120</a>
                    </li>
                    <li>
                        <a href="#!">Made with <font-awesome-icon class="footer__bottom-icon" :icon="['fas', 'heart']" />  By ThemeRage</a>
                    </li>
                    <li><a href="#!"></a></li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.footer {
    font-family: var(--f_Uniform);
    margin-bottom: 30px;

    .container {
        .footer__top {
            display: flex;
            align-items: start;
            justify-content: space-between;

            .title {
                color: var(--black);
            }

            .footer__list-first {
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                justify-content: center;

                h2 {
                    margin-bottom: 18px;
                }

                .socials {
                    display: flex;
                    column-gap: 8px;
                    margin-bottom: 15px;

                    .footer__link-social {
                        color: var(--icon);
                        font-size: 19px;
                        transition: .5s ease-in-out;

                        &:hover {
                            color: var(--link-hover);
                            transform: rotate(360deg);
                        }
                    }
                }

                li {
                    display: flex;
                    align-items: center;
                    column-gap: 10px;
                    margin-bottom: 27px;

                    .footer__link {
                        color: #4D606E;
                        font-size: 15px;
                        font-weight: 500;
                        transition: .5s;

                        &:hover {
                            color: var(--link-hover);
                        }
                    }

                    .footer__link-icon {
                        color: var(--icon);
                        transition: .5s ease-in-out;

                        &:hover {
                            color: var(--link-hover);
                            transform: rotate(360deg);
                        }
                    }
                }
            }

            .footer__list-second {
                display: flex;
                flex-direction: column;
                row-gap: 15px;
                h2 {
                    margin-bottom: 30px;
                }

                .footer__list-second-link {
                    color: var(--black);
                    font-size: 15px;
                    font-weight: 500;
                    transition: .5s;

                    &:hover {
                        color: var(--link-hover);
                    }
                }
            }

            .footer__list-third {
                display: flex;
                flex-direction: column;
                row-gap: 15px;

                h2 {
                    margin-bottom: 30px;
                }

                .footer__list-third-link {
                    color: var(--black);
                    font-size: 15px;
                    font-weight: 500;
                    transition: .5s;

                    &:hover {
                        color: var(--link-hover);
                    }
                }
            }

            .footer__list-fourth {
                h2 {
                    margin-bottom: 30px;
                }

                span {
                    color: #828282;
                    font-size: 15px;
                    font-weight: 500;
                }
                .footer__app-link {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    column-gap: 10px;
                    border: 2px solid var(--black);
                    border-radius: 15px; 
                    margin: 20px 0;
                    
                    
                        .footer__app-icon {
                        font-size: 45px;
                    }
                    .footer__app-info {
                        display: flex;
                        flex-direction: column;
                        align-items: flex-start;
                        padding: 5px;
                    }
                }
            }
        }
    }
}

.footer__bottom {
    border-top: 1px solid #BDBDBD;
    ul {
        display: flex;
        justify-content: space-between;
        margin-top: 30px;
        li {
            display: flex;
            column-gap: 10px;
            a {
                font-size: 15px;
                font-weight: 500;
                color: var(--black);
                span {
                    color: var(--link-hover);
                }
                .footer__bottom-icon {
                    color: var(--icon);
                    transition: .5s;
                    &:hover {
                        color: var(--link-hover);
                        transform: rotate(360deg);
                    }
                }
            }
        }
    }
}</style>