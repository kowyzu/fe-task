<template>
  <section id="section-pricing" class="section">
    <div class="container">
      <div class="row justify-content-center text-center">
        <div class="col-md-6 col p-4 p-md-0 pricing-heading">
          <h3>Plans & Pricing</h3>
          <h5>Startup Framework is free forever — you only pay for custom domain hosting or to export your site.</h5>
        </div>
      </div>
      <div class="row justify-content-center row-cols-1 row-cols-md-3 p-4 p-md-0 ">
        <div class="col pricing-table mb-4 mb-md-0">
          <PricingTableHeading :planName="starterPlanData.name" :planPrice="starterPlanData.price" />
          <ul class="p-0">
            <PricingTableItem v-for="(item) in starterPlanData.features" :key="item.id"
              :class="item.isChecked ? 'checked-list-item' : 'list-item'" :text="item.text"
              :isChecked="item.isChecked" />
          </ul>
          <div class="row justify-content-center">
            <button class="btn-action btn-big mt-4">Get Started</button>
          </div>
        </div>
        <div class="col pricing-table mx-md-4 mx-0 mb-4 mb-md-0">
          <PricingTableHeading :planName="professionalPlanData.name" :planPrice="professionalPlanData.price" />
          <ul class="p-0">
            <PricingTableItem v-for="(item) in professionalPlanData.features" :key="item.id"
              :class="item.isChecked ? 'checked-list-item' : 'list-item'" :text="item.text"
              :isChecked="item.isChecked" />
          </ul>
          <div class="row justify-content-center">
            <button class="btn-action btn-big mt-4">Get Started</button>
          </div>
        </div>
        <div class="col pricing-table">
          <PricingTableHeading :planName="teamPlanData.name" :planPrice="teamPlanData.price" />
          <ul class="p-0">
            <PricingTableItem v-for="(item) in teamPlanData.features" :key="item.id"
              :class="item.isChecked ? 'checked-list-item' : 'list-item'" :text="item.text"
              :isChecked="item.isChecked" />
          </ul>
          <div class="row justify-content-center m-0 p-0">
            <button class="btn-action btn-big mt-3">Get Started</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import PricingTableItem from './PricingTableItem.vue';
import PricingTableHeading from './PricingTableHeading.vue';

//Text
import text_JSON from './pricing.json'

export default {
  components: {
    PricingTableItem,
    PricingTableHeading
  },
  data() {
    return {
      starterPlanData: text_JSON[0],
      professionalPlanData: text_JSON[1],
      teamPlanData: text_JSON[2],
    }
  },
};


</script>