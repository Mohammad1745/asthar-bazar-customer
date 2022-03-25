<template>
  <div :class="className" class="filter">
    <DepartmentFilter className="" />
    <div class="flex justify-end gap-5">
      <ProductSorting />
      <FilterByCategory />
      <FilterByType />
    </div>
  </div>
</template>

<script>
import DepartmentFilter from "./product_filter/DepartmentFilter";
import ProductSorting from "./product_filter/ProductSorting";
import FilterByCategory from "./product_filter/FilterByCategory";
import FilterByType from "./product_filter/FilterByType";

export default {
  name: "FilterProducts",
  components: {FilterByType, FilterByCategory, DepartmentFilter, ProductSorting},
  props: ['className'],
  data(){
    return {
      departments: [
        {id:0, name: "Groceries", selected: true},
        {id:1, name: "Fish & Shrimp", selected: false},
      ]
    }
  }
}
</script>

<style scoped>
.filter {
  background: #f6f8fa;
  padding: 2rem 5rem;
  display: flex;
  justify-content: space-between;
  gap: 1rem;
}

@media (max-width: 990px){
  .filter {
    flex-direction: column;
  }
}
</style>
