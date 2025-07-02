<script setup>
// import HeroNavigation from './components/hero/HeroNavigation.vue';
// import HeroSlider from './components/hero/HeroSlider.vue';
// import FeaturesSlider from './components/features/FeaturesSlider.vue';
import HeroView from './components/hero/HeroView.vue';
import FeaturesView from './components/features/FeaturesView.vue';
</script>

<template>
  <header>
    <HeroView />
  </header>

  <main>
    <FeaturesView />
    <section id="section-call-to-action" class="section"></section>
    <section id="section-contact" class="section"></section>
    <section id="section-pricing" class="section"></section>

  </main>

  <footer>
    <!-- footer placeholder -->
  </footer>
</template>
