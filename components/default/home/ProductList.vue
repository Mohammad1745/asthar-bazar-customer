<template>
  <div :class="className">
    <div class="mx-10 flex flex-wrap  justify-around">
      <div
        v-for="i in 10"
        :key="i"
        class="product m-5 shadow-xl cursor-pointer">
        <div class="image">
          <img src="~assets/images/product_9.jpg" class="w-80 h-80" alt="">
        </div>
        <div class="name m-5 flex justify-center text-lg font-bold">
          বাগদা - বড় সাইজ (হিমায়িত)
        </div>
        <div class="price m-5 flex justify-center text-xl font-bold">
          49.99tk/kg
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductList",
  props: ['className'],
  data(){
    return {

    }
  }
}
</script>

<style scoped>
.product {
  transition: 0.5s;
}
.product:hover {
  transform: scale(1.1);
}
</style>
