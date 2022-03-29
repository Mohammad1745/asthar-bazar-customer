<template>
  <div :class="className" class="explanation-wrapper">
    <div class="explanation">
      <h2 class="explanation__header">How ?</h2>
      <div class="explanation__list">
        <div class="explanation__list__item">
          Whenever you or your referral purchases any thing from us, a portion of our profit will be saved in your WALLET.
          You may purchase our product with that. We have amazing Wallet Subscription Packages for you.
          We are offering Bronze package completely free for you. You may subscribe to other packages for larger wallet.
          Every wallet has 1 year lifespan. For users registered with referral code will be offered Golden wallet subscription
          free for first 12 months. After expiring, your wallet will be automatically renewed to existing package or smaller
          depending on amount of money present on your wallet. Or, You may subscribe to another before expire date.
        </div>
        <div class="explanation__list__item">
          <p>কিভাবে?</p>
          <p>
            আপনি অথবা আপনার রেফারেল আমাদের থেকে কোন জিনিস কিনলে আমাদের প্রফিটের একটি অংশ আপনার WALLET এ জমা হবে। পরবর্তিতে আপনি তা ব্যাবহার
            করে আমাদের থেকে কেনা কাটা করতে পারবেন। আমাদের কাছে আপনার জন্য দুর্দান্ত ওয়ালেট সাবস্ক্রিপশন প্যাকেজ রয়েছে।
            আমরা আপনার জন্য সম্পূর্ণ বিনামূল্যে ব্রোঞ্জ প্যাকেজ অফার করছি। বড় ওয়ালেটের জন্য আপনি অন্যান্য
            প্যাকেজগুলিতে সাবস্ক্রাইব করতে পারেন। প্রতিটি ওয়ালেটের মেয়াদ 1 বছর।রেফারেল কোড সহ নিবন্ধিত ব্যবহারকারীদের প্রথম 12 মাসের
            জন্য বিনামূল্যে গোল্ডেন ওয়ালেট সাবস্ক্রিপশন দেওয়া হবে। মেয়াদ শেষ হওয়ার পরে, আপনার মানিব্যাগটি স্বয়ংক্রিয়ভাবে চলমান অথবা ছোট
            প্যাকেজে পুনর্নবীকরণ হবে আপনার ওয়ালেটে উপস্থিত অর্থের উপর নির্ভর করে। অথবা, মেয়াদ শেষ হওয়ার আগে আপনি অন্য প্যাকেজে সাবস্ক্রাইব করতে পারেন।
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
