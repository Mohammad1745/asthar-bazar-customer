<template>
 <thead>
  <tr>
    <th
      v-for="(header, i) in headers"
      :key="i"
      :class="'th th'+i"
    >
      {{ header }}
    </th>
  </tr>
 </thead>
</template>

<script>
export default {
  name: "TableHeader",
  props: ['className'],
  data(){
    return {
      headers: ["Product", "Department", "Type", "Price", "Quantity", "Total"]
    }
  },
}
</script>

<style scoped>
 tr {
   display: flex;
   justify-content: space-between;
   background: #edf4f6;
   padding: 1rem 2.5rem;
 }
 .th {
   flex-basis: 0;
   flex-grow: 1;
   display: flex;
   justify-content: center;
 }
 .th0 {
   flex-grow: 2;
   justify-content: flex-start;
 }
</style>
