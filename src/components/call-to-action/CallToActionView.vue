<script setup>
import arrowIcon from '../../images/arrow-icon.svg'
</script>

<template>
  <section id="section-call-to-action" class="section">
    <div class="container">
      <div class="row text-center justify-content-center align-content-center">
        <div class="col-8">
          <h2>Easy to setup.<br>Easy to maintain</h2>
          <h5>
            Bootstrap is a widely-used, sleek, intuitive and powerful front-end framework for faster and easier web
            development.
          </h5>

          <div class="row justify-content-center mt-4">
            <div class="col-auto">
              <form action="#footer">
                <button class="btn-socials btn-big" type="submit">
                  <img class="p-3" :src="arrowIcon" alt="icon of arrow" />
                </button>
              </form>
            </div>
            <div class="col-auto">
              <form action="#section-contact">
                <button class="btn-action m-0" type="submit">Get Started</button>
              </form>
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>