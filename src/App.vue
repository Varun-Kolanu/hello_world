<template>
  <h2>{{ count }}</h2>
  <button v-on:click="count += 1">Increment</button>
  <button @click="decrement">Decrement</button> <!-- shorthand for v-on: is @ -->
  <button @click="clickHandler">Click</button>
  <button @click="clickHandler2(1,$event)">Click2</button>
  <button @click="decrement(), clickHandler($event)">Multiple methods</button> <!-- You should call the functions if are passing multiple methods and pass $event if event is used -->


</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      count: 0
    };
  },
  methods: {
    decrement() {
      this.count -= 1
    },
    clickHandler(event) {
      console.log(event) //event is automatically passed if no args passed
    },
    clickHandler2(x,event) {
      console.log(event) // $event needs to be passed if args passed
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
