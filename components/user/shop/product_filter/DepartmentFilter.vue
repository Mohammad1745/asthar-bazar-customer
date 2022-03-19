<template>
  <div :class="className" class="flex gap-2">
    <button
      v-for="department in departments"
      :key="department.id"
      :class="{selected: department.selected}"
      class="department"
    >{{ department.name }}</button>
  </div>
</template>

<script>
export default {
  name: "DepartmentFilter",
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
.department{
  padding: 0.5rem 1.5rem;
  border: 2px solid #bbe432;
  transition: 0.15s;
}
.department:hover{
  background: #bbe432;
}
.selected{
  background: #bbe432;
}
</style>
