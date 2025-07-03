<script setup>
import HeroView from './components/hero/HeroView.vue';
import FeaturesView from './components/features/FeaturesView.vue';
import CallToActionView from './components/call-to-action/CallToActionView.vue';
import ContactView from './components/contact/ContactView.vue';
</script>

<template>
  <header>
    <HeroView />
  </header>

  <main>
    <FeaturesView />
    <CallToActionView />
    <ContactView />


    <section id="section-pricing" class="section"></section>

  </main>

  <footer id="footer">
    <!-- footer placeholder -->
  </footer>
</template>
