<template>
  <div>
    <div class="chart">
      <BarChart :styles="myStyles" />
    </div>
    <div class="chart">
      <BarChart2 :styles="myStyles" />
    </div>
    <div class="chart">
      <LineChart :styles="myStyles" />
    </div>
    <div class="chart2">
      <DoughnutChart :styles="myStyles" />
    </div>
  </div>
</template>



<script>
import BarChart from '~/components/BarChart.vue';
import BarChart2 from '~/components/BarChart2.vue';
import LineChart from '~/components/LineChart.vue';
import DoughnutChart from '~/components/DoughnutChart.vue';

export default {
  components: {
    BarChart,
    LineChart,
    BarChart2,
    DoughnutChart,
  },
  data(){
    return{
      height:100
    }
  },
  computed:{
    myStyles(){
      return{
        height: `${this.height}%`,
        position:'relative'
      }
    }
  }
}
</script>


<style>
.chart {
  padding: 10px 30px;
  margin:10px;
  width:500px;
  height:300px;
  border:1px solid black;
  border-radius: 10px;
}

.chart2 {
  display:flex;
  padding: 10px 30px;
  margin:10px;
  width:500px;
  height:300px;
  border:1px solid black;
  border-radius: 10px;
}
</style>