<template>
  <div class="swiper swiper-features">
    <div class="swiper-wrapper">
      <div v-for="(slide, index) in textJson" :key="slide.id"
        class="swiper-slide features-swiper-slide px-md-5 px-0 row">
        <div class="slider-features-item text-start row px-5 px-md-0 ">
          <div class="row justify-content-lg-center">
            <div class="col-lg-8 col mt-5 pt-md-0">
              <h3>{{ slide.featuresTitle }}</h3>
              <h5>
                {{ slide.featuresDescription }}
              </h5>
            </div>
          </div>
          <div class="row row-cols-md-2 row-cols-1 justify-content-lg-center">
            <div class="col-lg-6 col features-block">
              <img :src="pagesIcon" alt="icon of pages" class="features-icon">
              <div class="label">{{ slide.featuresFirstBlock.label }}</div>
              <p>{{ slide.featuresFirstBlock.description }}</p>
            </div>
            <div class="col-lg-6 col features-block mt-4 mt-md-0">
              <img :src="symbolIcon" alt="icon of pages" class="features-icon">
              <div class="label">{{ slide.featuresSecondBlock.label }}</div>
              <p>{{ slide.featuresSecondBlock.description }}</p>
            </div>
          </div>
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
import pagesIcon from '../../images/pages-icon.svg'
import symbolIcon from '../../images/symbol-icon.svg'


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
      pagesIcon,
      symbolIcon
    }
  },
  methods: {
    initializeSwiper() {
      const swiper = new Swiper('.swiper-features', {
        direction: 'vertical',
        loop: true,

        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },

        autoplay: {
          delay: 5000,
        },
        slidesPerView: 1,
        spaceBetween: 15,
      });
    }
  },
};
</script>