<template>
  <div>
    <canvas id="chart-test" height="90"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js'
import ChartTestConfig from './chart-test-config'

export default {
  name: 'ChartTest',
  data() {
    return {
      chartData: ChartTestConfig.ChartTestData,
      chartOptions: ChartTestConfig.ChartTestOptions
    }
  },
  mounted() {
    const ctx = document.getElementById('chart-test');
    new Chart(ctx, this.chartData, this.chartOptions);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>