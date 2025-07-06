<script setup>
import ContactText from './ContactText.vue';
import ContactForm from './ContactForm.vue';
</script>

<template>
  <section id="section-contact" class="section">
    <div class="container-fluid">
      <div class="row row-cols-xl-2 row-cols-1 text-start justify-content-center">
        <div class="col-xl-6 col contact-text p-xl-0 p-5">
          <ContactText />
        </div>
        <div class="col-xl-6 col p-xl-0 p-md-5 p-3 ">
          <ContactForm />
        </div>
      </div>
    </div>
  </section>
</template>