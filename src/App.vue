<template>
  <About/>
</template>

<script>
import About from './views/About.vue'

export default {
  name: 'App',
  components: {
    About
  }
}

window.addEventListener('contextmenu', function (e) { 
  e.preventDefault(); 
}, false);

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
