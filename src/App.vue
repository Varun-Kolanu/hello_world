<template>
  <!-- should not mix v-if with v-for because v-if is computed before v-for. So use template tag -->

  <!-- Wrong: -->
  <!-- <div v-for="name in names" :key="name" v-if="name === 'Varun'">{{ name }}</div> -->

  <!-- Correct: -->
  <template v-for="name in names" :key="name" >
    <div v-if="name === 'Varun'">{{ name }}</div>
  </template>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      
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
