<template>
  <div>
    <h1>Agent Use (Last 20 Games)</h1>
    <BarChart></BarChart>
  </div>
  <div>
    <h2>Win/Lose Ratio (Last 20 Games)</h2>
    <PieChart></PieChart>
  </div>
</template>

<script>
import BarChart from './components/BarChart.vue';
import PieChart from './components/PieChart.vue'

export default {
  name: 'App',
  components: {
    BarChart,
    PieChart,
}
}    
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 60px;
}
</style>
