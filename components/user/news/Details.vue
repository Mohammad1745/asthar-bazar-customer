<template>
  <div :class="className" class="news">
    <div class="news__item">
      <div class="news__item__title">{{ news.title }}</div>
      <div class="news__item__date">Date: {{ news.date }}</div>
        <img src="~assets/images/home_slider_1.jpg" class="news__item__banner" alt="News">
      <div class="news__item__body">{{ news.body }}</div>
    </div>
  </div>
</template>

<script>


export default {
  name: "NewsDetails",
  props: ['className', 'news'],
  components: {},
  data(){
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.news {
  padding: 5vw 5vw 0 5vw;

  &__item {
    padding: 5vw;
    background-color: #edf4f6;
    display: flex;
    flex-direction: column;

    &__title {
      font-size: 1.5rem;
      font-weight: bold;
    }

    &__banner {
      margin: 1rem 0;
    }
  }
}
</style>
