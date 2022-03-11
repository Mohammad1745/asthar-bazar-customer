<template>
  <div class="">
    <Banner/>
    <ProductList className="mt-20"/>
  </div>
</template>

<script>
import Banner from "../components/default/home/Banner";
import ProductList from "../components/default/home/ProductList";

export default {
  name: 'IndexPage',
  components: {Banner, ProductList},
  data () {
    return {
    }
  }
}
</script>

<style scoped>

</style>
