<template>
  <div :class="className" class="product-table-wrapper">
    <table class="product-table">
      <TableHeader />
      <TableBody />
    </table>
    <TableButtons />
  </div>
</template>

<script>
import TableHeader from "./product_table/TableHeader";
import TableBody from "./product_table/TableBody";
import TableButtons from "./product_table/TableButtons";

export default {
  name: "ProductTable",
  props: ['className'],
  components: {TableHeader, TableBody, TableButtons},
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
  border-bottom: 1px solid #888;
}
@media (max-width:765px){
  .product-table-wrapper{
    width: 100vw;
    overflow-x: scroll;
  }
  .product-table{
    width: 766px;
  }
}

::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background: #dfdfdf;
  border-radius:10px;
}
::-webkit-scrollbar-thumb {
  background: #bbb;
  border-radius:10px;
}
::-webkit-scrollbar-thumb:hover {
  background: #888;
}
</style>
