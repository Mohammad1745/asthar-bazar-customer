<template>
  <div :class="className" class="coupon">
    <h2 class="coupon__header">Coupon Code</h2>
    <div class="coupon__input">
      <input type="text" v-model="code" class="coupon__input__field">
      <button class="coupon__input__button">Apply Coupon</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Coupon",
  props: ['className'],
  data() {
    return {
      code: ""
    }
  }
}
</script>

<style lang="scss" scoped>
  .coupon {
    &__header{
      font-size: 1.5rem;
      font-weight: bold;
      margin-bottom: 1.5rem;
    }

    &__input{
      display:flex;
      justify-content: flex-start;

      &__button{
        padding: 0 1.5rem;
        background: #bbe432;
        font-size: 1rem;
        text-transform: uppercase;
        color: #414141;
        font-weight: bold;
        transition: 0.15s;

        &:hover {
          background: #414141;
          color: #bbe432;
        }
      }
    }
  }
</style>
