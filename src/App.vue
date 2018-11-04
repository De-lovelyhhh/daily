<template>
  <div id="app">
    <nameList/>
  </div>
</template>

<script>
import nameList from './components/nameList.vue'
export default {
  name: 'App',
  components: {
    nameList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  /*-webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;*/
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
