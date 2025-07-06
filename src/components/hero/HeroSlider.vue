<template>
  <div class="swiper swiper-hero">
    <div class="swiper-wrapper">
      <div v-for="(slide, index) in textJson" :key="slide.id" class="swiper-slide">
        <div class="slider-hero-item text-center px-md-0 px-5 mb-5">
          <span class="hero-subtitle">{{ slide.heroSubtitle }}</span>
          <h1>{{ slide.heroTitle }}</h1>
          <h5 class="px-md-5 px-lg-0 px-0">
            {{ slide.heroDescription }}
          </h5>
        </div>
      </div>
    </div>
    <div class="swiper-pagination"></div>
    <div class="swiper-button-prev d-lg-block d-none"></div>
    <div class="swiper-button-next d-lg-block d-none"></div>
  </div>
</template>


<script>
//Swiper
import Swiper from 'swiper/bundle';
import 'swiper/css/bundle';

//Text
import text_JSON from './hero-slider.json'

export default {
  mounted() {
    this.initializeSwiper();
  },
  components: {
    Swiper
  },
  data() {
    return {
      textJson: text_JSON,
    }
  },
  methods: {
    initializeSwiper() {
      const swiper = new Swiper('.swiper-hero', {
        direction: 'horizontal',
        loop: true,

        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },

        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },

        autoplay: {
          delay: 5000,
        },
      });
    }
  },
};
</script>