<template>
  <div id="app">
    <Welcome/>
    <Stats/>
  </div>
</template>

<script>
import Welcome from './components/Welcome.vue'
import Stats from './components/Stats.vue'

export default {
  name: 'App',
  components: {
    Welcome,
    Stats,
  }
}
</script>

<style>
@import './reset.scss';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50; 
  box-sizing: border-box;
}
</style>
