<template>
  <div :class="className" class="details-wrapper">
    <div class="details">
      <h2 class="details__header">Account <span class="text-sm text-gray-500">(click titles to open)</span></h2>
      <div class="details__list">
        <NuxtLink
          v-for="(info, i) in infos"
          :key="i"
          :to="info.url"
          class="details__list__item">
          <div class="details__list__item__title">{{ info.title }}</div>
          <div class="details__list__item__amount">{{ info.value }}</div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PriceCalculation",
  props: ['className', 'infos'],
  data() {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
.details-wrapper{
  padding-top: 5vw;
}
.details {
  margin: 0 5vw;
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
      border: 2px solid transparent;
      border-radius: 2rem;
      transition:
        0.25s all ease-in;

      &__title {
        color: green;
      }

      &:last-child {
        background: white;
      }
      &:hover {
        border-color: #bbe432;
        background-color: rgba(0, 128, 0, 0.1);
      }
    }
  }
}
</style>
