<template>
  <tr>
    <td class="td td-name"><img src="~assets/images/product_9.jpg" class="w-12 h-12 mr-4" alt=""> {{ product.name }} - {{ product.variation }}</td>
    <td class="td">{{ product.department }}</td>
    <td class="td">{{ product.type }}</td>
    <td class="td">৳ {{ product.price }}</td>
    <td class="td td-quantity">
      <button @click="decreaseQuantity">-</button>
      <span>{{ product.quantity }}</span>
      <button @click="increaseQuantity">+</button>
    </td>
    <td class="td">৳ {{ product.totalPrice }}</td>
  </tr>
</template>

<script>
export default {
  name: "TableDataRow",
  props: ['product'],
  methods: {
    increaseQuantity(){
      this.$emit('quantity-increment')
    },
    decreaseQuantity(){
      this.$emit('quantity-decrement')
    }
  }
}
</script>

<style scoped>
tr {
  display: flex;
  justify-content: space-between;
  padding: 0.25rem 2.5rem;
}
.td {
  flex-basis: 0;
  flex-grow: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
.td-name {
  flex-grow: 2;
  justify-content: flex-start;
  font-size: 1.25rem;
  font-weight: bold;
}
.td-quantity button,
.td-quantity span {
  background: #edf4f6;
  padding: 0.5rem;
}
</style>
