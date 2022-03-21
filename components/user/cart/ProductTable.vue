<template>
  <div :class="className" class="product-table-wrapper">
    <table class="product-table">
      <TableHeader />
    </table>
  </div>
</template>

<script>
import TableHeader from "./product_table/TableHeader";

export default {
  name: "ProductTable",
  props: ['className'],
  components: {TableHeader},
  data(){
    return {
    }
  }
}
</script>

<style scoped>
.product-table-wrapper {
  padding: 5vw;
}
.product-table{
  width: 100%;
}
</style>
