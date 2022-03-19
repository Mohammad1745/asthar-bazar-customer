<template>
  <div class="">
    <Header/>
    <FilterProducts className=""/>
    <ProductList user="true" className="pt-20"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>
import ProductList from "../components/default/home/ProductList";
import Summary from "../components/default/home/Summary";
import Header from "../components/user/shop/Header";
import FilterProducts from "../components/user/shop/ProductFilter";

export default {
  name: 'ShopPage',
  layout: 'user',
  head:{
    title: "Home - Asthar Bazar - Promises 100% Reliance"
  },
  components: { Header, FilterProducts, ProductList, Summary },
  data () {
    return {
    }
  }
}
</script>

<style scoped>

</style>
