<script setup>
import HeroNavigation from './HeroNavigation.vue';
import HeroSlider from './HeroSlider.vue';
</script>

<template>
  <section id="section-hero" class="section">
    <div class="container-md container-fluid">
      <HeroNavigation />
      <HeroSlider />
      <form class="pb-5 pb-md-0" action="#section-contact">
        <button class="btn-action btn-middle" type="submit">Create an account</button>
      </form>
    </div>
  </section>
</template>