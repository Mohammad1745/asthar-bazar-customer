<template>
  <div :class="className" class="price">
    <h2 class="price__header">Cart Total</h2>
    <div class="price__calculations">
      <div class="price__calculation">
        <div class="price__calculation__title">Subtotal</div>
        <div class="price__calculation__amount">৳  {{ subtotal }}</div>
      </div>
      <div class="price__calculation">
        <div class="price__calculation__title">Coupon</div>
        <div class="price__calculation__amount">৳  {{ coupon }}</div>
      </div>
      <div class="price__calculation price__calculation--total">
        <div class="price__calculation__title">Subtotal</div>
        <div class="price__calculation__amount">৳  {{ subtotal }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PriceCalculation",
  props: ['className'],
  data() {
    return {
      subtotal: 294,
      coupon: 10,
      totalPrice: 284
    }
  }
}
</script>

<style lang="scss" scoped>
  .price {
    margin-top: 5rem;

    &__header{
      font-size: 1.5rem;
      font-weight: bold;
      margin-bottom: 2.5rem;
    }
    &__calculations {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin-bottom: 5rem;

      .price__calculation {
        display: flex;
        justify-content: space-between;
        font-size: 0.9rem;
        font-weight: 600;

        &--total{
          background: white;
          padding: 0.5rem 2rem;
          margin-left: -2rem;
          margin-right: -2rem;
        }
      }
    }
  }
</style>
