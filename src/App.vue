<template>
  <h2 v-once="name">{{ name }}</h2> 
  <!-- doesn't change after rendering once -->
  <button @click="name = 'Haha'">Change</button>

  <h2 v-pre>{{ name }}</h2>
  <!-- v-pre prevents compiling data variables -->
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'Varun'
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
