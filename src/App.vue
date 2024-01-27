<template>
  <Article title="Article Component" :likes="5" id="my-article" /> 
</template>

<script>
import Greet from './components/Greet.vue';
import Article from './components/Article.vue';

export default {
  name: 'App',
  components: {
    Greet, Article
  },
  data() {
    return {
      name: 'Dynamic'
    };
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
