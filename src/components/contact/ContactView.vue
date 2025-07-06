<script setup>
import ContactText from './ContactText.vue';
import ContactForm from './ContactForm.vue';
</script>

<template>
  <section id="section-contact" class="section">
    <div class="container-fluid">
      <div class="row row-cols-lg-2 row-cols-1 text-start justify-content-center">
        <div class="col-lg-6 col contact-text p-lg-0 p-5">
          <ContactText />
        </div>
        <div class="col-lg-6 col p-lg-0 p-md-5 p-3 ">
          <ContactForm />
        </div>
      </div>
    </div>
  </section>
</template>