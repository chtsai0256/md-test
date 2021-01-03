/* eslint-disable vue/no-unused-components */
<template>
  <div id="app">
    <meditor msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import meditor from './components/meditor.vue'

export default {
  name: 'App',
  components: {
    meditor,
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
