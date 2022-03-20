<template>
  <div class="">
    <Header title="Shop" :pages="pages"/>
    <FilterProducts className=""/>
    <ProductList user="true" className="pt-20"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>
import ProductList from "../components/default/ProductList";
import Summary from "../components/default/Summary";
import Header from "../components/default/Header";
import FilterProducts from "../components/user/shop/ProductFilter";

export default {
  name: 'ShopPage',
  layout: 'user',
  head:{
    title: "Shop - Asthar Bazar - Promises 100% Reliance"
  },
  components: { Header, FilterProducts, ProductList, Summary },
  data () {
    return {
      pages: [
        {name: "Home /", url: "/home"},
        {name: "Shop", url: "/shop"},
      ]
    }
  }
}
</script>

<style scoped>

</style>
