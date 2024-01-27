<template>
  <h2>App Username: {{ name }}</h2>
  <CompA />
</template>

<script>
import Greet from './components/Greet.vue';
import Article from './components/Article.vue';
import CompA from './components/CompA.vue';

export default {
  name: 'App',
  components: {
    Greet, Article, CompA
  },
  data() {
    return {
      name: 'Varun'
    };
  },
  provide() {
    return {
      username: this.name
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
