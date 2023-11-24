<template>
  <header class="header">
    <div class="header__desktop">
      <div class="header__desktop__top">
        <div class="header__desktop__top__items">
          <div class="header__desktop__top__item">
            <img
              src="../assets/check.svg"
              alt="check"
              class="header__desktop__top__item__icon"
            />
            <div class="header__desktop__top__item__text">
              30-DAY SATISFACTION GUARANTEE
            </div>
          </div>
          <div class="header__desktop__top__item">
            <img
              src="../assets/truck.svg"
              alt="check"
              class="header__desktop__top__item__icon"
            />
            <div class="header__desktop__top__item__text">
              Free delivery on orders over $40.00
            </div>
          </div>
          <div class="header__desktop__top__item">
            <img
              src="../assets/heart.svg"
              alt="check"
              class="header__desktop__top__item__icon"
            />
            <div class="header__desktop__top__item__text">
              50.000+ HAPPY CUSTOMERS
            </div>
          </div>
          <div class="header__desktop__top__item">
            <img
              src="../assets/arrows-check.svg"
              alt="check"
              class="header__desktop__top__item__icon"
            />
            <div class="header__desktop__top__item__text">
              100% Money Back Guarantee
            </div>
          </div>
        </div>
      </div>
      <div class="header__desktop__bottom">
        <div class="header__desktop__bottom__items">
          <div class="header__desktop__bottom__left">
            <a
              href="https://clarifion.com/"
              class="header__desktop__bottom__left__link"
            >
              <img
                src="../assets/clarifon.jpg"
                alt="clarifon"
                class="header__desktop__bottom__left__link__img"
              />
            </a>
          </div>
          <div class="header__desktop__bottom__right">
            <a
              href="https://www.mcafee.com/es-co/index.html"
              target="_blank"
              class="header__desktop__bottom__right__link"
            >
              <img
                src="../assets/mcafee.jpg"
                alt="mcafee"
                class="header__desktop__bottom__right__link__img"
              />
            </a>
            <a
              href="https://us.norton.com/"
              target="_blank"
              class="header__desktop__bottom__right__link"
            >
              <img
                src="../assets/norton.jpg"
                alt="norton"
                class="header__desktop__bottom__right__link__img"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="header__mobile">
      <div class="header__mobile__top">
        <button class="header__mobile__top__button" ref="$prev">
          <img
            src="../assets/left-arrow.svg"
            alt="left arrow"
            class="header__mobile__top__button__icon"
          />
        </button>
        <div class="header__mobile__top__slider" ref="sliderRef">
          <div class="header__mobile__top__slider__item">
            <img
              src="../assets/check.svg"
              alt="check"
              class="header__mobile__top__slider__item__icon"
            />
            <div class="header__mobile__top__slider__item__text">
              30-DAY SATISFACTION GUARANTEE
            </div>
          </div>
          <div class="header__mobile__top__slider__item">
            <img
              src="../assets/truck.svg"
              alt="check"
              class="header__mobile__top__slider__item__icon"
            />
            <div class="header__mobile__top__slider__item__text">
              Free delivery on orders over $40.00
            </div>
          </div>
          <div class="header__mobile__top__slider__item">
            <img
              src="../assets/heart.svg"
              alt="check"
              class="header__mobile__top__slider__item__icon"
            />
            <div class="header__mobile__top__slider__item__text">
              50.000+ HAPPY CUSTOMERS
            </div>
          </div>
          <div class="header__mobile__top__slider__item">
            <img
              src="../assets/arrows-check.svg"
              alt="check"
              class="header__mobile__top__slider__item__icon"
            />
            <div class="header__mobile__top__slider__item__text">
              100% Money Back Guarantee
            </div>
          </div>
        </div>
        <button class="header__mobile__top__button" ref="$next">
          <img
            src="../assets/right-arrow.svg"
            alt="right arrow"
            class="header__mobile__top__button__icon"
          />
        </button>
      </div>
      <div class="header__mobile__bottom">
        <div class="header__mobile__bottom__items">
          <div class="header__mobile__bottom__items__left">
            <a
              href="https://clarifion.com/"
              class="header__mobile__bottom__items__left__link"
            >
              <img
                src="../assets/clarifon-mobile.jpg"
                alt="clarifon"
                class="header__mobile__bottom__items__left__link__img"
              />
            </a>
          </div>
          <div class="header__mobile__bottom__items__right">
            <a
              href="https://www.mcafee.com/es-co/index.html"
              target="_blank"
              class="header__mobile__bottom__items__right__link"
            >
              <img
                src="../assets/mcafee-mobile.jpg"
                alt="mcafee"
                class="header__mobile__bottom__items__right__link__img"
              />
            </a>
            <a
              href="https://us.norton.com/"
              target="_blank"
              class="header__mobile__bottom__items__right__link"
            >
              <img
                src="../assets/norton-mobile.jpg"
                alt="norton"
                class="header__mobile__bottom__items__right__link__img"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { onMounted, ref } from "vue";
import "slick-carousel/slick/slick.css";
import "slick-carousel/slick/slick-theme.css";
import $ from "jquery";
import "slick-carousel";

const sliderRef = ref();
const $next = ref();
const $prev = ref();

onMounted(() => {
  if (sliderRef.value) {
    $(sliderRef.value).slick({
      dots: false,
      autoplay: true,
      infinite: true,
      arrows: true,
      nextArrow: $next.value,
      prevArrow: $prev.value,
    });
  }
});
</script>

<style scoped>
.header {
}
.header__desktop {
}
.header__desktop__top {
  background-color: #252f3d;
  padding-top: 15px;
  padding-bottom: 15px;
  padding-left: 127px;
  padding-right: 127px;
  display: flex;
  justify-content: center;
}

.header__desktop__top__item {
  display: flex;
  align-items: center;
  gap: 10px;
}

.header__desktop__top__items {
  max-width: 1666px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.header__desktop__top__item__icon {
  width: 22px;
  height: 22px;
}
.header__desktop__top__item__text {
  color: #fff;
  font-family: "Manrope";
  font-size: 12px;
  font-style: normal;
  font-weight: 500;
  line-height: 100%; /* 12px */
  text-transform: uppercase;
}
.header__desktop__bottom {
  padding-left: 127px;
  padding-right: 127px;
  padding-top: 30px;
  padding-bottom: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.header__desktop__bottom__items {
  display: flex;
  width: 100%;
  max-width: 1666px;
  justify-content: space-between;
}

.header__desktop__bottom__right {
  display: flex;
  align-items: center;
  gap: 32px;
}

.header__desktop__bottom__right__link__img {
  transition-duration: 0.3s;
}
.header__desktop__bottom__right__link__img:hover {
  transform: scale(1.1);
}

.header__desktop__bottom__left__link__img {
  transition-duration: 0.3s;
}
.header__desktop__bottom__left__link__img:hover {
  transform: scale(1.1);
}
.header__mobile {
  display: none;
}
@media only screen and (max-width: 750px) {
  .header__desktop {
    display: none;
  }
  .header__mobile {
    display: block;
  }
  .header__mobile__top {
    background-color: #252f3d;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-left: 20px;
    padding-right: 20px;
    padding-top: 10px;
    padding-bottom: 10px;
  }
  .header__mobile__top__button {
    padding: 0;
    border: none;
    outline: none;
    background-color: transparent;
  }
  .header__mobile__top__button:focus,
  .header__mobile__top__button:active {
    border: none;
    outline: none;
  }

  .header__mobile__top__slider {
    width: calc(100% - 20px - 20px);
  }

  .header__mobile__top__slider__item {
    display: flex !important;
    align-items: center;
    justify-content: center;
    gap: 8px;
  }

  .header__mobile__top__slider__item__text {
    color: #fff;
    font-family: "Manrope";
    font-size: 12px;
    font-style: normal;
    font-weight: 500;
    line-height: 100%; /* 12px */
    text-transform: uppercase;
  }

  .header__mobile__bottom {
    padding: 20px;
  }

  .header__mobile__bottom__items {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .header__mobile__bottom__items__right {
    display: flex;
    align-items: center;
    gap: 16px;
  }
}
</style>
