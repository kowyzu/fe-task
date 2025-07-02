<script setup>
import HeroNavigation from './HeroNavigation.vue';
import HeroSlider from './HeroSlider.vue';
</script>

<template>
  <section id="section-hero" class="section">
    <div class="container">
      <HeroNavigation />
      <HeroSlider />
      <form action="#section-contact">
        <button class="btn-action btn-action-hero" type="submit">Create an account</button>
      </form>
    </div>
  </section>
</template>