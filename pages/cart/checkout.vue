<template>
  <div class="">
    <Header title="Checkout" :pages="pages"/>
    <div class="main bg-white flex justify-between gap-20">
      <BillingForm  class-name="flex-1" />
      <BillingDetails  class-name="flex-1" />
    </div>
    <Summary className="mt-20"/>
  </div>
</template>

<script>
import Header from "../../components/default/Header";
import Summary from "../../components/default/Summary";
import BillingDetails from "../../components/user/cart/chekout/BillingDetails";
import BillingForm from "../../components/user/cart/chekout/BillingForm";

export default {
  name: 'CheckoutPage',
  layout: 'user',
  head:{
    title: "Checkout - Asthar Bazar - Promises 100% Reliance"
  },
  components: {BillingForm, BillingDetails, Header, Summary },
  data () {
    return {
      pages: [
        {name: "Home /", url: "/home"},
        {name: "Cart /", url: "/cart"},
        {name: "Checkout", url: "/cart/checkout"},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
 .main {
   padding: 5vw;
 }
 @media (max-width:1499px) {
   .main {
     flex-direction: column;
   }
 }
</style>
