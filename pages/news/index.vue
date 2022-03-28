<template>
  <div class="">
    <Header title="News" :pages="pages"/>
    <NewsList  className="bg-white" :all-news="allNews"/>
    <Summary className="mt-20"/>
  </div>
</template>

<script>

import Header from "../../components/default/Header";
import Summary from "../../components/default/Summary";
import NewsList from "../../components/user/news/NewsList";

export default {
  name: 'NewsPage',
  layout: 'user',
  head:{
    title: "News - Asthar Bazar - Promises 100% Reliance"
  },
  components: {Header, Summary, NewsList },
  data () {
    return {
      pages: [
        {name: "Home /", url: "/home"},
        {name: "News", url: "/news"},
      ],
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
