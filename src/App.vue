<template>
  <h2 v-if="num > 0">The num is positive</h2>
  <h2 v-else-if="num === 0">The number is zero</h2>
  <h2 v-else>The number is negative</h2>

  <template v-if="display">  <!-- this is not rendered as a seperate div -->
    <h2>Hi</h2>
    <h2>Hello</h2>
    <h2>Hey</h2>
  </template>

  <h2 v-show="show">v-show</h2>  <!-- v-show adds 'display: none' if set to false but v-if removes the element itself from the DOM -->
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      num: 0,
      display: true,
      show: false
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
