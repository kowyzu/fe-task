<template>
  <div class="pricing-table-heading">
    <h5>{{ planName }}</h5>
    <h2>{{ planPrice }}<sup class="currency ms-2">$</sup></h2>
  </div>
</template>

<script>
export default {
  props: {
    planName: String,
    planPrice: Number
  }
}
</script>