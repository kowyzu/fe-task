<script setup>
import FeaturesSlider from './FeaturesSlider.vue';
import notebookImage from '../../images/notebook.webp';
</script>

<template>
  <section id="section-features" class="section">
    <img class="img-notebook d-xl-block d-none" :src="notebookImage" alt="half of notebook displaying styles">
    <div class="container-fluid">
      <div class="row h-100 align-items-stretch">
        <div class="col-xl-4 col-12"></div>
        <FeaturesSlider class="col-xl-8 col-12 d-flex flex-column me-md-5 me-0" />
      </div>
    </div>
  </section>
</template>