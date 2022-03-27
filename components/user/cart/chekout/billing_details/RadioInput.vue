<template>
  <div :class="className" class="radio-input">
    <h2 class="radio-input__header">{{ header }}</h2>
    <div class="radio-input__options">
      <div
        v-for="option in options"
        :key="option.id"
        class="radio-input__option">
        <input type="radio" v-model="selectedOption" :value="option.value" class="radio-input__option__input">
        <span class="radio-input__option__title">{{ option.title }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RadioInput",
  props: ['className', 'header', 'options', 'default'],
  data() {
    return {
      selectedOption: this.default
    }
  }
}
</script>

<style lang="scss" scoped>
  .radio-input {
    margin-top: 5rem;

    &__header{
      font-size: 1.5rem;
      font-weight: bold;
      margin-bottom: 2.5rem;
    }
    &__options {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin-bottom: 5rem;
    }
    &__option {
      display: flex;
      justify-content: flex-start;
      gap: 1rem;
      font-size: 0.9rem;
      font-weight: 600;
    }
  }
</style>
