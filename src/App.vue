<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import './assets/css/reset.css'
export default {
  name:'app'
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height:100vh;
  overflow:auto;
  margin:0 auto;
  padding-bottom: 4.2857rem;
  color: #2c3e50;
}
</style>
