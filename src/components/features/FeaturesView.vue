<script setup>
import FeaturesSlider from './FeaturesSlider.vue';
import notebookImage from '../../images/notebook.webp';
</script>

<template>
  <section id="section-features" class="section">
    <img class="img-notebook  d-lg-block d-none" :src="notebookImage" alt="half of notebook displaying styles">
    <div class="container-fluid">
      <div class="row h-100 align-items-stretch">
        <div class="col-lg-4 col-0"></div>
        <FeaturesSlider class="col-lg-8 col d-flex flex-column me-md-5 me-0" />
      </div>
    </div>
  </section>
</template>