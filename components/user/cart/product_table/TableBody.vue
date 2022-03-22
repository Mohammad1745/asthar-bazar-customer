<template>
  <tbody class="mt-3">
    <TableDataRow
      v-for="product in products"
      :key="product.id"
      :product="product"
      @quantity-increment="increaseQuantity(product.id)"
      @quantity-decrement="decreaseQuantity(product.id)"
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
      products: [
        {id: 0, name: 'বাগদা', variation: 'বড় সাইজ', type: 'হিমায়িত', department: 'Fish & Shrimp', image: '~assets/images/product_9.jpg', price: 49.99, quantity: 3, totalPrice: 149.97},
        {id: 1, name: 'বাগদা', variation: 'ছোট সাইজ', type: 'হিমায়িত', department: 'Fish & Shrimp', image: '~assets/images/product_9.jpg', price: 49.99, quantity: 1, totalPrice: 49.99},
      ]
    }
  },
  methods: {
    increaseQuantity(id){
      this.products.filter(product => product.id === id).forEach(product => {
        product.quantity++
        product.totalPrice = (product.price * product.quantity).toFixed(2)
      })
    },
    decreaseQuantity(id){
      this.products.filter(product => product.id === id).forEach(product => {
        product.quantity--
        product.totalPrice = (product.price * product.quantity).toFixed(2)
      })
    }
  }
}
</script>

<style scoped>
</style>
