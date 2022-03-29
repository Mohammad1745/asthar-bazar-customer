<template>
  <div class="">
    <Header title="Account" :pages="pages"/>
    <Details class-name="bg-white" :infos="infos"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>
import Header from "../../components/default/Header";
import Summary from "../../components/default/Summary";
import Details from "../../components/user/account/index/Details";


export default {
  name: 'AccountPage',
  layout: 'user',
  head:{
    title: "Account - Asthar Bazar - Promises 100% Reliance"
  },
  components: {Header, Summary, Details },
  data () {
    return {
      pages: [
        {name: "Home", url: "/account"},
      ],
      infos: [
        {title: "Profile", value: "25%", url: "/account/profile"},
        {title: "Referral", value: "5", url: "/account"},
        {title: "Wallet", value: "৳  25", url: "/account"},
        {title: "Orders", value: "10", url: "/account"},
      ]
    }
  }
}
</script>

<style scoped>

</style>
