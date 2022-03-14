<template>
  <div :class="className">
    <div class="parallax-background">
      <img src="/categories.jpg" alt="" class="">
    </div>
    <div class="parallax-window">
      <div class="page">Shop</div>
      <div class="directory text-gray-500">
        <NuxtLink class="text-md py-4" to="/home">
          Home
        </NuxtLink>/
        <NuxtLink class="text-md py-4" to="/shop">
          Shop
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ['className'],
  data(){
    return {

    }
  }
}
</script>

<style scoped>

.parallax-window
{
  background: transparent;
  height: 25rem;
  padding: 8vw 10vw;
  z-index:2;
}
.parallax-background
{
  position: absolute;
  top: 0;
  right: 0;
  min-height: 25rem;
  width:100%;
  z-index:-1;
}
.parallax-background img
{
  width:100%;
}
@media (max-width: 1199px){
  .parallax-background {
    width:1200px;
  }
}
.page{
  font-weight: 300;
  font-size: 72px;
}
</style>
