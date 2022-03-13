<template>
  <div class="">
    <ProductList className="mt-20"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>
import Banner from "../components/default/home/Banner";
import ProductList from "../components/default/home/ProductList";
import Summary from "../components/default/home/Summary";

export default {
  name: 'ShopPage',
  layout: 'user',
  head:{
    title: "Home - Asthar Bazar - Promises 100% Reliance"
  },
  components: { Banner, ProductList, Summary },
  data () {
    return {
    }
  }
}
</script>

<style scoped>

</style>
