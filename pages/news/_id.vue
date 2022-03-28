<template>
  <div class="">
    <Header title="News" :pages="pages"/>
    <News v-if="this.news" className="bg-white" :news="news"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>

import Header from "../../components/default/Header";
import Summary from "../../components/default/Summary";
import News from "../../components/user/news/Details";

export default {
  name: 'NewsDetailsPage',
  layout: 'user',
  head:{
    title: "News - Asthar Bazar - Promises 100% Reliance"
  },
  components: {Header, Summary, News },
  data () {
    return {
      pages: [
        {name: "Home /", url: "/home"},
        {name: "News /", url: "/news"},
      ],
      news: null,
      allNews: [
        {
          id: 0,
          title: 'Something is happening1',
          date: '2021-08-26',
          body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra temp or so dales. Phasellus sagittis auctor gravida. Integ er bibendum sodales arcu id te mpus. Ut consectetur lacus.'
        },
        {
          id: 1,
          title: 'Something is happening2',
          date: '2021-08-26',
          body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra temp or so dales. Phasellus sagittis auctor gravida. Integ er bibendum sodales arcu id te mpus. Ut consectetur lacus.'
        },
        {
          id: 2,
          title: 'Something is happening3',
          date: '2021-08-26',
          body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra temp or so dales. Phasellus sagittis auctor gravida. Integ er bibendum sodales arcu id te mpus. Ut consectetur lacus.'
        },
      ]
    }
  },
  beforeMount() {
    let id = 1
    console.log(id, "id")
    this.news = this.allNews.find(item => item.id === id)
    this.pages.push({name: this.news.title, url: ""})
    console.log(this.news, "news")
  }
}
</script>

<style lang="scss" scoped>
 .main {
   padding: 5vw;
 }
 @media (max-width:1499px) {
   .main {
     flex-direction: column;
   }
 }
</style>
