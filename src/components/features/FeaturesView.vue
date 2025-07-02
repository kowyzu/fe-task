<script setup>
import FeaturesSlider from './FeaturesSlider.vue';
import notebookImage from '../../images/notebook.webp';
</script>

<template>
  <section id="section-features" class="section">
    <img class="img-notebook  d-md-block d-none" :src="notebookImage" alt="half of notebook displaying styles">
    <div class="container-fluid">
      <div class="row h-100 align-items-stretch">
        <div class="col-md-4 col-0"></div>
        <FeaturesSlider class="col-md-8 d-flex flex-column me-md-5 me-0" />
      </div>
    </div>
  </section>
</template>