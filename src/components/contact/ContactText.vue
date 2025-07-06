<script setup>
import phoneIcon from '../../images/phone-icon.svg'
import buildingIcon from '../../images/building-icon.svg'
import envelopeIcon from '../../images/envelope-icon.svg'
</script>

<template>
  <div class="container">
    <h3>Let’s Keep in Touch</h3>
    <h5>We have created a new product that will help designers, developers and companies create websites for
      their startups quickly and easily.</h5>
    <ul class="list-unstyled">
      <li class="d-flex align-items-start">
        <img :src="phoneIcon" alt="icon of phone" class="me-3" width="24" height="24" />
        <p>+1 555 505 5050</p>
      </li>
      <li class="d-flex align-items-start">
        <img :src="envelopeIcon" alt="icon of envelope" class="me-3" width="24" height="24" />
        <p>info@designmodo.com</p>
      </li>
      <li class="d-flex align-items-start">
        <img :src="buildingIcon" alt="icon of building" class="me-3" width="24" height="24" />
        <p>
          San Francisco, CA 560 Bush St & 20th Ave, Apt 5 San Francisco, 230909
        </p>
      </li>
    </ul>
  </div>
</template>