<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from '@/components/home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
html, body {
  height: 100%;
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 60px;
}
</style>
