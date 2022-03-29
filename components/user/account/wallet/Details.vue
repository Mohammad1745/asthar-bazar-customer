<template>
  <div :class="className" class="details-wrapper">
    <div class="details">
      <h2 class="details__header">Wallet</h2>
      <div class="details__list">
        <div
          v-for="(info, i) in wallet"
          :key="i"
          class="details__list__item">
          <div class="details__list__item__title">{{ info.title }}</div>
          <div class="details__list__item__amount">{{ info.value }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WalletDetails",
  props: ['className', 'wallet'],
  data() {
    return {
    }
  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>
.details-wrapper{
  padding: 5vw;
}
.details {
  padding: 5vw;
  background: #edf4f6;

  &__header{
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 2.5rem;
  }
  &__list {
    display: flex;
    flex-direction: column;
    gap: 1rem;

    &__item {
      display: flex;
      justify-content: space-between;
      padding: 0.5rem 2rem;
      margin-left: -2rem;
      margin-right: -2rem;
      font-size: 0.9rem;
      font-weight: 600;
      border-radius: 2rem;

      &:last-child {
        background: white;
        font-weight: bold;
      }
    }
  }
}

</style>
