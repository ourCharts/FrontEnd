<template>
  <div id="app">
    <el-container style="height: 100%">
        <el-aside><amenu @added="hello"></amenu></el-aside>
        <el-main>
          <Map :prop1=xx :prop2=yy></Map>
        </el-main>
    </el-container>
  </div>
</template>

<script>
import Map from './components/map'
import amenu from './components/menu'
export default {
  name: 'App',
  data () {
    return {
      xx: 'asd',
      yy: 'king'
    }
  },
  methods: {
    hello: function (data1, data2) {
      // alert(data1)
      // alert(data2)
      this.xx = data1
      this.yy = data2
    }
  },
  components: {
    Map, amenu
  }

}
</script>

<style>
  html,
  body {
    height: 100%;
    width: 100%;
    margin: 0;
    background-color: #545c64;
  }

  .anchorBL {
    display: none;
  }

  .el-main {
    padding: 0;
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
