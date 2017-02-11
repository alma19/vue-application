<template>
  <div id="app">
    <Slider></Slider>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Slider from './components/Slider'

export default {
  name: 'app',
  components: {
    Hello,
    Slider
  }
}
</script>

<style>
body {
  background-color: black; 
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
