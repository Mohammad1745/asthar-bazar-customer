<template>
  <div :class="className" class="price-summary">
    <Coupon />
  </div>
</template>

<script>
import Coupon from "./price_summary/Coupon";

export default {
  name: "PriceSummary",
  props: ['className'],
  components: {Coupon},
}
</script>

<style lang="scss" scoped>
  .price-summary {
    margin: 0 5vw;
    padding: 5vw;
    background: #edf4f6;
  }
</style>
