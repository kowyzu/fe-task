<script setup>
import ContactText from './ContactText.vue';
</script>

<template>
  <section id="section-contact" class="section">
    <div class="container-fluid">
      <div class="row text-start justify-content-center">
        <div class="col-6 contact-text p-0">
          <ContactText />
        </div>
        <div class="col-6 p-0 ">
          <div class="contact-form container">
            <div class="row">
              <div class="col">
                <input type="text" class="form-control" placeholder="First name" aria-label="First name">
              </div>
              <div class="col">
                <input type="text" class="form-control" placeholder="Last name" aria-label="Last name">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>