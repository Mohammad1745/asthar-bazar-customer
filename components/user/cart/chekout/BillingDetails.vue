<template>
  <div :class="className" class="billing-details">
    <PriceCalculation />
    <div class="grid grid-cols-2">
      <RadioInput header="Payment Options" :options="paymentOptions" :default="paymentOptions[0].value"/>
      <RadioInput header="Shipping Methods" :options="shippingMethods" :default="shippingMethods[0].value" />
    </div>
  </div>
</template>

<script>

import PriceCalculation from "../index/price_summary/PriceCalculation";
import RadioInput from "./billing_details/RadioInput";

export default {
  name: "PriceSummary",
  props: ['className'],
  components: {RadioInput, PriceCalculation},

  data(){
    return {
      paymentOptions: [
        {id: 0, value: 'bkash', title: 'BKASH'},
        {id: 1, value: 'bank', title: 'Bank'},
        {id: 2, value: 'cod', title: 'Cash On Delivery'},
      ],
      shippingMethods: [
        {id: 0, value: 'sa_paribahan', title: 'SA Paribahan'},
        {id: 1, value: 'sundarban_courier', title: 'Sundarban Curier'},
      ],
    }
  }
}
</script>

<style lang="scss" scoped>
  .billing-details {
    padding: 0 5vw;
    background: #edf4f6;
  }
</style>
