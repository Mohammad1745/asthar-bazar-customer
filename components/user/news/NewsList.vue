<template>
  <div :class="className" class="news">
    <div
      v-for="news in allNews"
      :key="news.id"
      class="news__list">
      <div class="news__list__item">
        <div class="news__list__item__title">{{ news.title }}</div>
        <div class="news__list__item__date">Date: {{ news.date }}</div>
        <NuxtLink :to="'/news/details'+news.id">
          <img src="~assets/images/home_slider_1.jpg" class="news__list__item__banner" alt="News">
        </NuxtLink>
        <div class="news__list__item__body">{{ news.body.substring(0,100) }}...</div>
        <NuxtLink :to="'/news/details'+news.id" class="news__list__item__details-btn">Read more...</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: "ProductTable",
  props: ['className', 'allNews'],
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

  &__list{
    display: flex;
    flex-direction: column;
    border-bottom: 4px solid #414141;

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

      &__details-btn {
        margin-top: 1rem;
        color: #bbe432;
      }
    }
  }
}
@media (max-width:765px){
  .news{
    max-height: 100vh;
    overflow-y: scroll;
  }
}

::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background: #dfdfdf;
  border-radius:10px;
}
::-webkit-scrollbar-thumb {
  background: #bbb;
  border-radius:10px;
}
::-webkit-scrollbar-thumb:hover {
  background: #888;
}
</style>
