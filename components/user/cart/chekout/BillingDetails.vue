<template>
  <div :class="className" class="price-summary">
    <PriceCalculation />
  </div>
</template>

<script>

import PriceCalculation from "../index/price_summary/PriceCalculation";

export default {
  name: "PriceSummary",
  props: ['className'],
  components: {PriceCalculation},
}
</script>

<style lang="scss" scoped>
  .price-summary {
    padding: 0 5vw;
    background: #edf4f6;
  }
</style>
