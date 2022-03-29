<template>
  <tbody class="mt-3">
    <TableDataRow
      v-for="subPackage in packages"
      :key="subPackage.id"
      :sub-package="subPackage"
    />
  </tbody>
</template>

<script>
import TableDataRow from "./table_body/TableDataRow";

export default {
  name: "TableDataRows",
  props: ['className'],
  components: {TableDataRow},
  data(){
    return {
      packages: [
        {id: 0, name: "Bronze", charge: 0, capacity: 100, subscribed: true},
        {id: 0, name: "Silver", charge: 25, capacity: 250, subscribed: false},
        {id: 0, name: "Golden", charge: 50, capacity: 500, subscribed: false},
        {id: 0, name: "Titanium", charge: 100, capacity: 1000, subscribed: false},
        {id: 0, name: "Platinum,", charge: 250, capacity: 2500, subscribed: false},
        {id: 0, name: "Zirconium", charge: 500, capacity: 5000, subscribed: false},
        {id: 0, name: "Uranium", charge: 1000, capacity: 10000, subscribed: false},
      ]
    }
  },
  methods: {
  }
}
</script>

<style scoped>
</style>
