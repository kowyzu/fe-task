<template>
  <div class="swiper swiper-features">
    <div class="swiper-wrapper">
      <div v-for="(slide, index) in textJson" :key="slide.id" class="swiper-slide px-5">
        <div class="slider-hero-item text-center">
          <span class="hero-subtitle">{{ slide.heroSubtitle }}</span>
          <h1>{{ slide.heroTitle }}</h1>
          <h5>
            {{ slide.heroDescription }}
          </h5>
        </div>
      </div>
    </div>
    <div class="swiper-pagination"></div>
  </div>
</template>


<script>
//Swiper
import Swiper from 'swiper/bundle';
import 'swiper/css/bundle';

//Text
import text_JSON from './features-slider.json'

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
      const swiper = new Swiper('.swiper-features', {
        direction: 'vertical',

        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },

        autoplay: {
          delay: 5000,
        },
      });
    }
  },
};
</script>