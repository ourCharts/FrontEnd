<template>
  <div ref="map" style="height: 400px; width: 600px;"></div>
</template>

<script>
import echarts from 'echarts'
import 'echarts/extension/bmap/bmap.js'
export default {
  name: 'Map',
  data () {
    return {
      msg: 'hello',
      chart: echarts.ECharts
    }
  },
  methods: {
    init: function () {
      this.chart = echarts.init(this.$refs.map)
      let options = {
        bmap: {
          center: [120.13066322374, 30.240018034923],
          zoom: 10,
          roam: true
        },
        series: [{
          type: 'scatter',
          coordinateSystem: 'bmap',
          data: [
            [120.13066322374, 30.240018034923],
            [120, 30],
            [119.8, 29.989]
          ]
        }]
      }
      console.log('debug: ' + this.chart)
      this.chart.setOption(options)
      let bmap = this.chart.getModel().getComponent('bmap').getBMap()
      bmap.addControl(new BMap.MapTypeControl())
    }
  },
  mounted () {
    this.init()
  }
}
</script>

<style>

</style>
