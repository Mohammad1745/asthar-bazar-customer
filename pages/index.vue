<template>
  <div class="">
    <Banner/>
    <ProductList className="mt-20"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>
import Banner from "../components/default/home/Banner";
import ProductList from "../components/default/ProductList";
import Summary from "../components/default/Summary";

export default {
  name: 'IndexPage',
  head:{
    title: "Home - Asthar Bazar - Promises 100% Reliance"
  },
  components: {Banner, ProductList, Summary},
  data () {
    return {
    }
  }
}
</script>

<style scoped>

</style>
