<template>
  <h2>Volume (0-20): {{ volume }}</h2>
  <button @click="volume += 2">Increase</button>
  <button @click="volume -= 2">Decrease</button>
  <input type="text" v-model="movie">

  <input type="number" v-model="info.age">
  <input type="text" v-model="info.name">
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      volume: 0,
      movie: 'Batman',
      info: {
        age: null,
        name: ''
      }
    };
  },
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert('Increasing Volume my damage hearing')
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API Call with movie: ${newValue}`);
      },
      immediate: true // Runs on page reload too
    },
    info: {
      handler(newValue) {
        console.log(`Info: Age = ${newValue.age}, Name = ${newValue.name}`)
      },
      deep: true //* Generally watchers aren't called if deep properties change in an object or array. If we use .concat, and change the array itself, deep true not required as whole array got changed
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
