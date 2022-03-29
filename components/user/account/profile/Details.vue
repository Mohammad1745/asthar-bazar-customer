<template>
  <div :class="className" class="details-wrapper">
    <div class="details">
      <h2 class="details__header">Profile</h2>
      <div class="details__list">
        <div
          v-for="(info, i) in infos"
          :key="i"
          class="details__list__item">
          <div class="details__list__item__title">{{ info.title }}</div>
          <div class="details__list__item__amount">{{ info.value }}</div>
        </div>
      </div>
    </div>
    <div class="details-buttons">
      <button
        @click="setProfileEditMode"
        class="details-buttons__button bg-green text-sm uppercase font-bold px-5 py-3">Edit Profile</button>
      <button
        @click="setPasswordEditMode"
        class="details-buttons__button bg-green-inverted text-sm uppercase font-bold px-5 py-3">Edit Password</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "PriceCalculation",
  props: ['className', 'infos'],
  data() {
    return {
      subtotal: 294,
      coupon: 10,
      totalPrice: 284
    }
  },
  methods: {
    setProfileEditMode(){
      this.$emit('profile_edit_mode', true)
    },
    setPasswordEditMode(){
      this.$emit('password_edit_mode', true)
    },
  }
}
</script>

<style lang="scss" scoped>
.details-wrapper{
  padding: 5vw;

  .details-buttons {
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

  @media (max-width: 765px) {
    .details-buttons {
      justify-content: flex-start;
    }
  }
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
      }
    }
  }
}

</style>
