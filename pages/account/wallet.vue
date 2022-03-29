<template>
  <div class="">
    <Header title="Wallet" :pages="pages"/>
    <Details class-name="bg-white" :wallet="wallet"/>
    <Explanation />
    <Summary className=""/>
  </div>
</template>

<script>
import Header from "../../components/default/Header";
import Summary from "../../components/default/Summary";
import Details from "../../components/user/account/wallet/Details";
import Explanation from "../../components/user/account/wallet/Explanation";


export default {
  name: 'WalletPage',
  layout: 'user',
  head:{
    title: "Wallet  - Asthar Bazar - Promises 100% Reliance"
  },
  components: {Header, Summary, Details, Explanation },
  data () {
    return {
      pages: [
        {name: "Account /", url: "/account"},
        {name: "Wallet", url: "/account/wallet"},
      ],
      wallet: [
        {title: "Subscribed Package", value: "Bronze"},
        {title: "Capacity", value: "৳ 100"},
        {title: "Cash", value: "৳ 0"},
        {title: "Expire Date", value: "2021-05-05"},
      ]
    }
  }
}
</script>

<style scoped>

</style>
