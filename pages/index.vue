<template>
  <div id="home">
    <!--<Hero />-->
    <div class="wrapper md:px-10 pt-10">
      <div class="header mt-5">
        <Introduction />
        <!--<News />-->
        <!--<full-calendar v-bind:event="items"/>-->
      </div>
      <div class="mt-16">
        <Products />
        <!--<Instagram />-->
        <LazyGooglemap />
        <Information />
        <!--<LazyTable />-->
        <LazySwiperimage />
      </div>
    </div>
  </div>
</template>

<script>
if (process.browser) { // Here we introduce... According to the environment wow.js
  var {WOW} = require('wowjs')
}
  // import Hero from '../components/Hero.vue'
  // import Introduction from '../components/Introduction.vue'
  // import News from '../components/News.vue'
  // import Social from '../components/Social.vue'
  // import Projects from '../components/Projects.vue'
  // import Information from '../components/Information.vue'
  // import Products from '../components/Products.vue'
  // import Googlemap from '../components/Googlemap.vue'
  // import Instagram from '../components/Instagram.vue'
  // import Table from '../components/Table.vue'
  // import Swiperimage from '../components/Swiperimage.vue'
  // import axios from 'axios'
  // import IntersectionObserver from "../components/IntersectionObserver"

    export default {
  //     components:{
  //       Introduction, News, Information, Social, Projects, Products, IntersectionObserver, Googlemap, Table, Swiperimage
  //     },
  //     // head() {
  //     //   return {
  //     //     script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
  //     //   };
  //     // },
  //     data() {
  //       return {
  //         items: []
  //       };
  //     },
  //     async asyncData({ $config }) {
  //       const { data } = await axios.get(
  //         $config.baseUrl,
  //         {
  //           headers: { "X-API-KEY": $config.apiKey }
  //         }
  //       );
  //       const events = []
  //       for (var i=0; i < data.contents.length ; ++i){
  //         let colors = ""
  //         switch(data.contents[i]['color'][0]) {
  //           case "紫":
  //             colors = '#FF99FF'
  //             break
  //           case "オレンジ":
  //             colors = '#FF9933'
  //             break
  //           case "青":
  //             colors = '#66CCFF'
  //             break
  //           case "緑":
  //             colors = '#66CC66'
  //             break
  //           default:
  //             colors = '#F0F0F0'
  //             break
  //         }
  //         let ev = {
  //           id : i,
  //           title : data.contents[i]['title'],
  //           start : data.contents[i]['eventDate'],
  //           detail : data.contents[i]['detail'],
  //           backgroundColor : colors
  //         }
  //         events.push(ev)
  //       }
  //       return {
  //         items: events
  //       };
  //     },
      mounted() {
        this.$nextTick(() => {
          if (process.browser) { // On the page mounted In the life cycle Instantiate according to the environment WOW
            new WOW({animateClass: 'animate__animated',live: false, }).init()
          }
        });
      },
    };
</script>

<style>

</style>