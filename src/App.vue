<template>
  <div id="app">
   <el-container style="height: 100%">
       <el-aside>
         <el-menu
          background-color="#545c64"
          text-color="#fff"
          active-text-color="#ffd04b">
          <el-menu-item index="1">
             <span slot="title">Info 1</span>
           </el-menu-item>
           <el-menu-item index="2">
            <span slot="title">Info 2</span>
           </el-menu-item>
           <el-menu-item index="3">
            <span slot="title">Info 3</span>
          </el-menu-item>
          <el-submenu index="4">
            <template slot="title">Group 1</template>
            <el-menu-item-group>
              <el-menu-item index="4-1">Option 1</el-menu-item>
              <el-menu-item index="4-2">Option 2</el-menu-item>
              <el-menu-item index="4-3">Option 3</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="5">
            <template slot="title">Group 2</template>
            <el-menu-item-group>
              <el-menu-item index="5-1">Option 1</el-menu-item>
              <el-menu-item index="5-2">Option 2</el-menu-item>
              <el-menu-item index="5-3">Option 3</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-container>
        <el-main>
          <Map></Map>
        </el-main>
      </el-container>
    </el-container>
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
