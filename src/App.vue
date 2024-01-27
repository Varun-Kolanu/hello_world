<template>
  <div :style="{
    color: highlightColor,
    fontSize: fontSize + 'px',
    border: '2px solid red'
  }">Css binding</div>
  <div :style="styleObject">Css Object Binding</div>
  <div :style="[baseStyleObject, backgroundStyleObject]">Array Style</div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      highlightColor: 'green',
      fontSize: 50,
      styleObject: {
        color: 'green',
        fontSize: '50px',
        border: '2px solid red'
      },
      baseStyleObject: {
        color: 'green'
      },
      backgroundStyleObject: {
        backgroundColor: 'lightblue'
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
