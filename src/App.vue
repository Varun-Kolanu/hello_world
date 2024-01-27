<template>
  <input type="text" placeholder="First Name" v-model.lazy="firstName">
  <h2>Full Name: {{ firstName }} {{ lastName }}</h2>
  <h2>Computed: {{ fullName }}</h2>
  <h2>Method Call: {{ getFullName() }}</h2>
  <input type="text" name="random" id="random" placeholder="Random UI Change" v-model="random">
  <!-- Computed properties are cached and only recalculated when one of the involved component change. But methods are recalled whenever a change in UI occurs -->
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Varun',
      lastName: 'Kolanu',
      random: ''
    };
  },
  methods: {
    getFullName() {
      console.log("Method Called")
      return `${this.firstName} ${this.lastName}`
    }
  },
  computed: {
    fullName() {
      console.log("Computed called")
      return `${this.firstName} ${this.lastName}` 
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
