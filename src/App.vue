<template>
  <button @click="changeFullName">Change Full Name</button>
  <h2>Full Name: {{ firstName }} {{ lastName }}</h2>
  <h2>Computed: {{ fullName }}</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Varun',
      lastName: 'Kolanu'
    };
  },
  methods: {
    changeFullName(value) {
      this.fullName = "Some Random"
    }
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}` 
      },
      set(value) {
        const names = value.split(' ');
        this.firstName = names[0];
        this.lastName = names[1];
      }
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
