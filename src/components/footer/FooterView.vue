<script setup>
import twitterIcon from '../../images/twitter-icon.svg'
import facebookIcon from '../../images/facebook-icon.svg'
import googleIcon from '../../images/google-icon.svg'
</script>

<template>
  <div class="container">
    <footer class="py-5">
      <div class="d-flex flex-column flex-sm-row justify-content-between py-md-2 my-md-2 py-1 my-1">
        <span class="col-md-4 mb-0 justify-content-start ps-2 ps-md-0">Startup 3</span>
        <ul class="nav col-md-4 justify-content-md-end">
          <li class="nav-item">
            <a href="#section-contact" class="nav-link px-2">
              <p>Privacy Policy</p>
            </a>
          </li>
          <li class="nav-item">
            <a href="#section-contact" class="nav-link px-2">
              <p>Terms</p>
            </a>
          </li>
          <li class="nav-item">
            <a href="https://x.com/" target="_blank" class="nav-link px-2"><img :src="twitterIcon"
                alt="icon of Twitter"></a>
          </li>
          <li class="nav-item">
            <a href="https://www.facebook.com/" target="_blank" class="nav-link px-2"><img :src="facebookIcon"
                alt="icon of Facebook"></a>
          </li>
          <li class="nav-item">
            <a href="https://www.google.com/" target="_blank" class="nav-link px-2"><img :src="googleIcon"
                alt="icon of Google"></a>
          </li>
        </ul>
      </div>
      <div class="d-flex flex-column flex-sm-row justify-content-between py-md-4 my-md-4 py-1 my-1 border-top">
        <ul class="nav col-md-6 justify-content-start">
          <li class="nav-item">
            <a href="#" class="nav-link px-2">
              <p>Tour</p>
            </a>
          </li>
          <li class="nav-item">
            <a href="#section-features" class="nav-link px-2">
              <p>Features</p>
            </a>
          </li>
          <li class="nav-item">
            <a href="#section-pricing" class="nav-link px-2">
              <p>Pricing Plans</p>
            </a>
          </li>
          <li class="nav-item">
            <a href="#section-features" class="nav-link px-2">
              <p>Our Works</p>
            </a>
          </li>
          <li class="nav-item">
            <a href="#section-call-to-action" class="nav-link px-2">
              <p>Brands</p>
            </a>
          </li>
          <li class="nav-item">
            <a href="#section-contact" class="nav-link px-2">
              <p>Contacts</p>
            </a>
          </li>
        </ul>
        <p class="nav col-md-4 justify-content-md-end ps-2 ps-md-0">© 2025. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>
