<template>
  <div id="app">
    <!-- <article-comp id="my-article" title='Article' :likes="50" :isPublished="false" /> -->
    <!-- <GreetComponent hero-name="batman" name="kavin"/>
    <GreetComponent hero-name="spiderman" name="sebastian"/>
    <GreetComponent :hero-name="chanel" :name="name"/> -->
    <button @click="showPopup = true" >Show Popup</button>
    <PopupComponent v-show="showPopup" @close="closePopup" />
  </div>
</template>

<script>
// import GreetComponent from './components/Greet.vue'
// import ArticleComp from './components/Article.vue'
import PopupComponent from './components/Popup.vue'
export default {
  name: 'App',
  components:{
    // GreetComponent,
    // ArticleComp,
    PopupComponent
  },
  data(){
    return{
      name: 'Kavin sebastian',
      chanel: 'kavin yeagers',
      showPopup: false
    }
  },
  methods:{
    closePopup(name){
      this.showPopup = false
      console.log('name', name)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
