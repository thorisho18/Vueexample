<template>
  <div id="app">
    <img alt="Vue logo" src="logo.png">
    <HelloWorld msg=""/>
       <Map/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Map from './components/map.vue'

export default {
  name: 'App',
  components: {
      Map
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
