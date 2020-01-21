<template>
  <div ref="map" id="map-container"></div>
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
      // eslint-disable-next-line
      bmap.addControl(new BMap.MapTypeControl())
      bmap.setMapStyleV2({
        styleId: '59a80bc22d507e09700207fce541bc16'
      })
    }
  },
  mounted () {
    this.init()
  }
}
</script>

<style>
#map-container {
  width: 100%;
  height: 100%;
  margin: 0;
}
</style>
