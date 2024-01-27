<template>
  <Greet name="Varun"/>
  <Greet name="Vishwak"/>
  <Greet :name="name" />
  <!-- v-bind for dynamic props -->
</template>

<script>
import Greet from './components/Greet.vue';
export default {
  name: 'App',
  components: {
    Greet,
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
