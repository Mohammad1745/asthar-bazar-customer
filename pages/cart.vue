<template>
  <div class="">
    <Header title="Cart" :pages="pages"/>
    <ProductTable  className="bg-white"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>
import Header from "../components/default/Header";
import Summary from "../components/default/Summary";
import ProductTable from "../components/user/cart/ProductTable";

export default {
  name: 'CartPage',
  layout: 'user',
  head:{
    title: "Cart - Asthar Bazar - Promises 100% Reliance"
  },
  components: { Header, ProductTable, Summary },
  data () {
    return {
      pages: [
        {name: "Home /", url: "/home"},
        {name: "Cart", url: "/cart"},
      ]
    }
  }
}
</script>

<style scoped>

</style>
