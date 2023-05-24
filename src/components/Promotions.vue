<script>

import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';




export default {
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
};
</script>


<template>
  <section class="promotions">
    <div class="container">
      <h2 class="promotions__title title">Hot<span class="title-span">Promotions</span></h2>
      <carousel :items-to-show="4" class="promotions__slider">
        <slide class="promotions__slide">
          <img src="../image/promotions/promotions-bg.png" alt="" class="promotions__image">
          <div class="promotions__content">
            <div class="promotions__timer">
              <div class="promotions__time">
                <p>Days</p>
                <span>01</span>
              </div>
              <div class="promotions__time">
                <p>Days</p>
                <span>01</span>
              </div>
              <div class="promotions__time">
                <p>Days</p>
                <span>01</span>
              </div>
              <div class="promotions__time">
                <p>Days</p>
                <span>01</span>
              </div>
            </div>
            <div class="promotions__footer">
              <h4>Seeds of Change Organic Quinoa,Brown,& Red Rice</h4>
              <div class="promotions__footer-stars">
                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                <button><font-awesome-icon :icon="['fas', 'star']" /></button>
                <button><font-awesome-icon style="color: var(--text);" :icon="['fas', 'star']" /></button>
                <span>(4.0)</span>
              </div>
              <div class="promotions__footer-price">
                <div>
                  <p>Piker per kg</p>
                  <p class="price">
                    <span>$24.00</span>
                    <del> $30.00</del>
                  </p>
                </div>
                <button>
                  <font-awesome-icon class="add-btn" :icon="['fas', 'cart-shopping']" />
                  <span>Add</span>
                </button>
              </div>
            </div>
          </div>
        </slide>

        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </div>
  </section>
</template>


<style lang="scss" scoped>
.promotions {
  .container {
    .promotions__slider {
      .promotions__slide {
        max-width: 570px;
        width: 100% !important;
        padding: 104px 60px;
        border-radius: 10px;
        overflow: hidden;
        text-align: left;
        
        .promotions__image {
          position: absolute;
          width: 100%;
          height: 100%;
          object-fit: cover;
        }

        .promotions__content {
          position: relative;
          z-index: 1;
          .promotions__timer {
            display: flex;
            column-gap: 10px;
            margin-bottom: 10px;
            justify-content: center;
            .promotions__time {
              max-width: 105px;
              width: 100%;
              padding: 10px 0;
              background: var(--white);
              border-radius: 10px;
              text-align: center;
              p {
                color: #2FD080;
                font-weight: 500;
              }
              span {
                font-size: 40px;
                font-weight: 500;
                color: var(--title);
              }
            }
          }
          .promotions__footer {
            background: var(--white);
            border-radius: 10px;
            padding: 20px;
            h4 {
              font-size: 19px;
              color: var(--title);
              margin-bottom: 5px;
            }
            .promotions__footer-stars {
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
            .promotions__footer-price {
              display: flex;
              align-items: center;
              justify-content: space-between;
              div {
                p {
                  font-size: 15px;
                  color: var(--text);
                }
                .price {
                  margin-top: 15px;
                  color: var(--title);
                  font-weight: 700;
                  del {
                    font-size: 14px;
                    font-weight: 400;
                    color: var(--text);
                  }
                }
              }
              button {
                width: 83px;
                padding: 12px 10px;
                border-radius: 5px;
                background: #D4EEE2;
                display: flex;
                justify-content: space-between;
                color: var(--link-hover);
                .add-btn {
                  font-size: 14px;
                  span {
                    font-size: 12px;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>