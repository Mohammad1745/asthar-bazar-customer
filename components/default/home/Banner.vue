<template>
  <div :class="className">
    <div class="content">
      <div class="discount">
        <div class="amount">{{ discount }}</div>
        <div class="percent">%</div>
        <div class="text1">upto</div>
        <div class="text2">Discount on the</div>
      </div>
      <div class="text3">New Collection</div>
      <NuxtLink class="shop-btn bg-green-inverted text-sm font-bold px-5 py-4" :to="buttonLink">
        SHOP NOW
      </NuxtLink>
    </div>
    <img :src="bannerImage" class="" alt="">
  </div>
</template>

<script>
export default {
  name: "Banner",
  props: ['className'],
  data(){
    return {
      discount: 5,
      buttonLink: 'signin',
      bannerImage: "/_nuxt/assets/images/home_slider_1.jpg"
    }
  }
}
</script>

<style scoped>
.content {
  position: relative;
  top: 5vw;
  height: 0;
}
.discount{
  display:grid;
  grid-template-areas:
      'number percent'
      'number text1'
      'number text2';
  max-width: 30vw;
  line-height: .75;
  color: #414141;
}
.amount{
  grid-area: number;
  font-size: 10vw;
  font-weight: bold;
  text-align: right;
}
.percent{
  grid-area: percent;
  font-size: 5vw;
  font-weight: bold;
}
.text1{
  grid-area: text1;
  font-size: 1.15vw;
}
.text2{
  grid-area: text2;
  font-size: 1.15vw;
}
.text3 {
  margin-left: 8vw;
  font-size: 5vw;
  font-weight: 300;
  color: #414141;
}
.shop-btn {
  margin-left: 8.5vw;
}
</style>
