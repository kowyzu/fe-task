<script setup>
import HeroNavigation from './components/hero/HeroNavigation.vue';
import HeroSlider from './components/hero/HeroSlider.vue';
import FeaturesSlider from './components/features/FeaturesSlider.vue';
</script>

<template>
  <header>
    <section id="section-hero" class="section">
      <div class="container">
        <HeroNavigation />
        <HeroSlider />
        <form action="#section-contact">
          <button class="btn-action btn-action-hero" type="submit">Create an account</button>
        </form>
      </div>
    </section>
  </header>

  <main>
    <section id="section-features" class="section">
      <img class="img-notebook" src="./images/notebook.webp" alt="half of notebook displaying styles">
      <div class="container-fluid">
        <div class="row h-100 align-items-stretch">
          <div class="col-md-4 col-0"></div>
          <FeaturesSlider class="col-8 d-flex flex-column me-5" />
        </div>
      </div>
    </section>
    <section id="section-call-to-action" class="section"></section>
    <section id="section-contact" class="section"></section>
    <section id="section-pricing" class="section"></section>

  </main>

  <footer>
    <!-- footer placeholder -->
  </footer>
</template>
