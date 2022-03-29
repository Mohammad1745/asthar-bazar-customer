<template>
  <div class="">
    <Header title="Referral" :pages="pages"/>
    <Details
      @generate_code="generateCode"
      class-name="bg-white"
      :code="referralCode"
      :count="referralCount"
    />
    <Summary className=""/>
  </div>
</template>

<script>
import Header from "../../components/default/Header";
import Summary from "../../components/default/Summary";
import Details from "../../components/user/account/referrals/Details";


export default {
  name: 'ProfilePage',
  layout: 'user',
  head:{
    title: "Profile - Asthar Bazar - Promises 100% Reliance"
  },
  components: {Header, Summary, Details },
  data () {
    return {
      pages: [
        {name: "Account /", url: "/account"},
        {name: "Referral", url: "/account/referral"},
      ],
      referralCode: null,
      referralCount: 0,
    }
  },
  methods: {
    generateCode (code) {
      this.referralCode = code
    }
  }
}
</script>

<style scoped>

</style>
