<template>
<div v-bind:id="heading">Heading</div> <!-- binds variable to an attribute such as id, disabled -->
<button :disabled="isDisabled">Bind</button> <!-- shorthand for v-bind -->
<h2 :class="status">Status</h2>
<h2 :class="isPromoted && 'promoted'">Promoted</h2>
<h2 :class="isSoldOut ? 'sold-out' : 'exists'">Sold Out ?</h2>
<h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'exists']">Array Conditional</h2>
<h2 :class="{
  promoted: isPromoted,
  exists: !isSoldOut,
  'sold-out': isSoldOut
}">Object binding</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Varun",
      branch: "<b>CSE</b>",
      heading: "heading",
      isDisabled: true,
      status: "success",
      isPromoted: true,
      isSoldOut: false
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

.success {
  background-color: green;
}

.promoted {
  background-color: lightblue;
}

.sold-out {
  color: red;
}

.exists {
  color: green;
}
</style>
