<template>
  <div :class="className" class="details-wrapper">
    <div class="details">
      <h2 class="details__header">Referral</h2>
      <div
        v-if="code"
        class="details__list"
      >
        <div class="details__list__item">
          <div class="details__list__item__title">Referral Code</div>
          <button
            @click="copy(code)"
            title="Click to Copy"
            class="details__list__item__button">
            {{ code }}
          </button>
        </div>
        <div class="details__list__item">
          <div class="details__list__item__title">My Referrals</div>
          <div class="details__list__item__amount">{{ count }}</div>
        </div>
      </div>
      <div v-else class="details__list">
        <div class="details__list__item">
          <div class="details__list__item__title">Referral Code</div>
          <button
            @click="generateCode"
            class="details__list__item__button">
            Generate Code
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ReferralDetails",
  props: ['className', 'code', 'count'],
  data() {
    return {
    }
  },
  methods: {
    async copy (text) {
      try {
        await this.$copyText(text)
        alert("Copied To Clipboard")
      } catch (e) {
        console.error(e);
      }
    },
    generateCode () {
      this.$emit('generate_code', 'X8F7cD6noJ')
    }
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
      }
      &__button {
        font-weight: bold;
        color: green;
      }
    }
  }
}

</style>
