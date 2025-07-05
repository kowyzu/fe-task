<template>
  <section id="section-pricing" class="section">
    <div class="container">
      <div class="row justify-content-center text-center">
        <div class="col-6 pricing-heading">
          <h3>Plans & Pricing</h3>
          <h5>Startup Framework is free forever — you only pay for custom domain hosting or to export your site.</h5>
        </div>
      </div>
      <div class="row justify-content-center gx-5">
        <div class="col-3 pricing-table">
          <div class="pricing-table-heading">
            <h5>Starter</h5>
            <h2>9.99<sup class="currency ms-2">$</sup></h2>
          </div>
          <ul class="p-0">
            <li class="checked-list-item">
              <span class="check-icon"></span>
              <p>2 GB of space</p>
            </li>
            <li class="checked-list-item">
              <span class="check-icon"></span>
              <p>14 days of backups</p>
            </li>
            <li class="checked-list-item">
              <span class="check-icon"></span>
              <p>Social integrations</p>
            </li>
            <li class="checked-list-item">
              <span class="check-icon"></span>
              <p>Client billing</p>
            </li>
            <li class="list-item">
              <p class="ps-4">Remote access</p>
            </li>
            <li class="list-item">
              <p class="ps-4">Custom domain</p>
            </li>
            <li class="list-item">
              <p class="ps-4">24 hours support</p>
            </li>
            <li class="list-item">
              <p class="ps-4">Admin tools</p>
            </li>
            <li class="list-item">
              <p class="ps-4">Collaboration tools</p>
            </li>
            <li class="list-item">
              <p class="ps-4">User management</p>
            </li>
          </ul>
          <div class="row justify-content-center">
            <button class="btn-action btn-big mt-4">Get Started</button>
          </div>
        </div>
        <div class="col-3 pricing-table">
          <div class="pricing-table-heading">
            <h5>Starter</h5>
            <h2>9.99<sup class="currency ms-2">$</sup></h2>
          </div>
          <ul>
            <div v-for="(item, index) in starterPlanData" :key="item.id">
              <PricingTableItem :class="item.isChecked ? 'checked-list-item' : 'list-item'" :text="item.text"
                :isChecked="item.isChecked" />
            </div>
          </ul>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
import PricingTableItem from './PricingTableItem.vue';

//Text
import text_JSON from './pricing.json'

export default {
  components: {
    PricingTableItem
  },
  data() {
    return {
      textJson: text_JSON,
      starterPlanData: text_JSON[0].features,
    }
  },
};


</script>