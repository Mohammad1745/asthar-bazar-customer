<template>
  <div :class="className" class="table-buttons">
    <NuxtLink class="table-buttons__button bg-green text-md font-bold px-5 py-4" to="/shop">
      Continue Shopping
    </NuxtLink>
    <button class="table-buttons__button bg-white text-md font-bold px-5 py-3">Clear Cart</button>
  </div>
</template>

<script>
export default {
  name: "TableButtons",
  props: ['className'],
}
</script>

<style lang="scss" scoped>
  .table-buttons {
    display: flex;
    justify-content: flex-end;
    gap: 1rem;
    margin: 1rem 0;

    .bg-white {
      background: #ddd;
      color: #414141;
      transition: 0.15s;

      &:hover {
        background: #414141;
        color: #fff;
      }
    }
  }
</style>
