<template>
  <div :class="className" class="explanation-wrapper">
    <div class="explanation">
      <h2 class="explanation__header">Why ?</h2>
      <div class="explanation__list">
        <div class="explanation__list__item">
          Anyone registered with your referral code will be your referral. Whenever he/she purchases any thing from us, you will receive a portion of our profit as you have helped us to reach that person. You will receive that on your WALLET. You may purchase our product with that.
        </div>
        <div class="explanation__list__item">
          <p>কেন?</p>
          <p>
            আপনার রেফারেল কোড ব্যাবহার করে কেউ রেজিস্ট্রেশন করলে তিনি আপনার রেফারেল হবে। তিনি আমাদের থেকে কোন জিনিস কিনলে আমাদের প্রফিটের একটি অংশ আপনি পাবেন যেহেতু আপনার মাধ্যমে তিনি আমাদের সাথে যুক্ত হয়েছেন।এটা আপনার WALLET এ জমা হবে। পরবর্তিতে আপনি তা ব্যাবহার করে আমাদের থেকে কেনা কাটা করতে পারবেন।
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ReferralExplanation",
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
.explanation-wrapper{
  padding: 0 5vw 5vw;
}
.explanation {
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
      font-size: 0.9rem;
      font-weight: 600;
    }
  }
}

</style>
