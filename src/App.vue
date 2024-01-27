<template>
<div> {{ greet }} {{ name }} </div>
<div v-text="branch" ></div> <!-- replaces whole varaible of v-text into the div's inner html -->
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Varun",
      branch: "CSE"
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
