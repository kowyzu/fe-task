<script setup>
import HeroView from './components/hero/HeroView.vue';
import FeaturesView from './components/features/FeaturesView.vue';
import CallToActionView from './components/call-to-action/CallToActionView.vue';
import ContactView from './components/contact/ContactView.vue';
import PricingView from './components/pricing/PricingView.vue';
import FooterView from './components/footer/FooterView.vue';
</script>

<template>
  <header>
    <HeroView />
  </header>

  <main>
    <FeaturesView />
    <CallToActionView />
    <ContactView />
    <PricingView />
  </main>

  <footer id="footer">
    <FooterView />
  </footer>
</template>
