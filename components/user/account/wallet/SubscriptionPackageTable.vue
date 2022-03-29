<template>
  <div :class="className" class="subscription-package-table-wrapper">
    <div class="header">Wallet Subscription Packages</div>
    <table class="subscription-package-table">
      <TableHeader />
      <TableBody />
    </table>
  </div>
</template>

<script>
import TableHeader from "./subscription_package_table/TableHeader";
import TableBody from "./subscription_package_table/TableBody";

export default {
  name: "ProductTable",
  props: ['className'],
  components: {TableHeader, TableBody},
  data(){
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.subscription-package-table-wrapper {
  padding: 5vw;

  .header {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 2.5rem;
  }
}
.subscription-package-table{
  width: 100%;
  border-bottom: 1px solid #888;
}
@media (max-width:765px){
  .subscription-package-table-wrapper{
    width: 100vw;
    overflow-x: scroll;
  }
  .subscription-package-table{
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
