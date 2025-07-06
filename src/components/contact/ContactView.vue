<script setup>
import ContactText from './ContactText.vue';
import ContactForm from './ContactForm.vue';
</script>

<template>
  <section id="section-contact" class="section">
    <div class="container-fluid">
      <div class="row text-start justify-content-center">
        <div class="col-md-6 col contact-text p-md-0 p-5">
          <ContactText />
        </div>
        <div class="col-md-6 col p-md-0 p-3">
          <ContactForm />
        </div>
      </div>
    </div>
  </section>
</template>