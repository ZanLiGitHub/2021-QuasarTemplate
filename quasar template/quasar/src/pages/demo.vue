<template>
<div>
  <div style="width: 500px; height: 500px;" ref="chartRef"></div>
</div>
</template>

<script>

//引入echarts
import * as echarts from 'echarts'

export default {
  name: 'echarts',
  data() {
    return {}
  },
  methods: {},
  mounted() {
    let myChart = echarts.init(this.$refs.chartRef);
    myChart.setOption({
      title: {
        text: 'ECharts 入门示例'
      },
      tooltip: {},
      xAxis: {
        data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子']
      },
      yAxis: {},
      series: [{
        name: '销量',
        type: 'bar',
        data: [5, 20, 36, 10, 10, 20]
      }]
    });
  },
}
</script>

<style scoped>

</style>
