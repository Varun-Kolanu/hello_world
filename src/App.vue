<template>
  <div v-for="name in names" :key="name">{{ name }}</div> <!-- creates multiple divs for each name. Similar to map in reactjs -->
  <!-- or  -->
  <div v-for="(name, index) in names" :key="index"> {{ index + 1 }}. {{ name }}</div>

  <div v-for="value in info" :key="value">{{ value }}</div>
  <div v-for="(value, key, index) in info" :key="index">{{ index }}. {{ key }}: {{ value }}</div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      names: ['Varun', 'Vishwak', 'Vishnu'],
      info: {
        name: 'Varun',
        age: 19
      }
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
