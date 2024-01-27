<template>
<div> {{ greet }} {{ name }} </div>
<div v-html="branch"></div> <!-- replaces whole html of v-html into the div's inner html and be cautious -->
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Varun",
      branch: "<b>CSE</b>"
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
