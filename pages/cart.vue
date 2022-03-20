<template>
  <div class="">
    <Header title="Cart" :pages="pages"/>

    <Summary className="mt-20"/>
  </div>
</template>

<script>
import ProductList from "../components/default/ProductList";
import Summary from "../components/default/Summary";
import Header from "../components/default/Header";
import FilterProducts from "../components/user/shop/ProductFilter";

export default {
  name: 'CartPage',
  layout: 'user',
  head:{
    title: "Cart - Asthar Bazar - Promises 100% Reliance"
  },
  components: { Header, FilterProducts, ProductList, Summary },
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
