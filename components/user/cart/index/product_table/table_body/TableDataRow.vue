<template>
  <tr>
    <td class="td td-name"><img src="~assets/images/product_9.jpg" class="w-12 h-12 mr-4" alt=""> {{ product.name }} - {{ product.variation }}</td>
    <td class="td">{{ product.department }}</td>
    <td class="td">{{ product.type }}</td>
    <td class="td">৳ {{ product.price }}</td>
    <td class="td td-quantity">
      <button @click="decreaseQuantity" class="iterator-button">-</button>
      <span>{{ product.quantity }}</span>
      <button @click="increaseQuantity" class="iterator-button">+</button>
    </td>
    <td class="td">৳ {{ product.totalPrice }}</td>
    <td class="td td-action">
      <button class="delete-button"><i class="fas fa-trash"></i></button>
    </td>
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

<style scoped lang="scss">
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

  &-name {
    flex-grow: 2;
    justify-content: flex-start;
    font-size: 1.25rem;
    font-weight: bold;
  }
  &-action{
    flex-grow: 0.25;
  }
}
.iterator-button,
.td-quantity span {
  background: #edf4f6;
  padding: 0.5rem;
}
.delete-button{
  transition: 0.25s;
}
.delete-button:hover{
  background: #edf4f6;
  padding: 0.5rem 0.8rem;
  border-radius: 50%;
}
</style>
