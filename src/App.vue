<template>
  <div id="app">
    <Map></Map>
  </div>
</template>

<script>
import Map from './components/map'
export default {
  name: 'App',
  components: {
    Map
  }
}
</script>

<style>
html, body {
  height: 100%;
  width: 100%;
  margin: 0;
}

.anchorBL {
  display: none;
}

#app {
  width: 100%;
  height: 100%;
  margin: 0;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
