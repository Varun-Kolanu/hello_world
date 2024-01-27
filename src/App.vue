<template>
  <h2>{{ 1 + 2 + 3 }}</h2>
  <h2>Add method: {{ add(1,2,3) }}</h2>
  <h2>Multiply: {{ multiplier(2,4) }}</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      
    };
  },
  methods: {
    add(a,b,c) {
      return a+b+c
    },
    multiplier: (x,y) => {
      return x*y
    }
    // If you use arrow function, cn't use this keyword to access data
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
