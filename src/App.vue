<script setup>
import HeroView from './components/hero/HeroView.vue';
import FeaturesView from './components/features/FeaturesView.vue';
import CallToActionView from './components/call-to-action/CallToActionView.vue';
</script>

<template>
  <header>
    <HeroView />
  </header>

  <main>
    <FeaturesView />
    <CallToActionView />

    <section id="section-contact" class="section"></section>
    <section id="section-pricing" class="section"></section>

  </main>

  <footer id="footer">
    <!-- footer placeholder -->
  </footer>
</template>
