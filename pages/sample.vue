<template>
  <div class="chart_con">
    <div class="chart">
      <BarChart :styles="myStyles" />
    </div>
    <div class="chart">
      <BarChart2 :styles="myStyles" />
    </div>
    <div class="chart">
      <BarChart3 :styles="myStyles" id="canvas" />
    </div>
    <div class="chart">
      <LineChart :styles="myStyles" />
    </div>
    <div class="chart2">
      <DoughnutChart :styles="myStyles1" />
      <DoughnutChart2 :styles="myStyles1" />
      <DoughnutChart3 :styles="myStyles1" />
    </div>
  </div>
</template>

<style>
.chart_con {
  display: flex;
  justify-content: center;
  flex-wrap:wrap;
  background:black;
}
.chart {
  padding: 10px 20px;
  margin: 1%;
  width: 40%;
  height: 300px;
  border: 1px solid blue;
  border-radius: 10px;

    @media screen and (max-width: 768px) {
      width: 80%;
    }

    @media screen and (max-width: 480px) {
      height: 200px;
    }
}

.chart2 {
  display: flex;
  padding: 10px 20px;
  margin: 1%;
  width: 40%;
  height: 300px;
  border: 1px solid blue;
  border-radius: 10px;

    @media screen and (max-width: 768px) {
      width: 80%;
    }

    @media screen and (max-width: 480px) {
      height: 200px;
    }
}

</style>

<script>
import BarChart from "~/components/BarChart.vue";
import BarChart2 from "~/components/BarChart2.vue";
import BarChart3 from "~/components/BarChart3.vue";
import LineChart from "~/components/LineChart.vue";
import DoughnutChart from "~/components/DoughnutChart.vue";

export default {
  components: {
    BarChart,
    BarChart2,
    BarChart3,
    LineChart,
    DoughnutChart,
  },
  data() {
    return {
      height: 100,
      width:33,
    };
  },
  computed: {
    myStyles() {
      return {
        height: `${this.height}%`,
        position: "relative",
      };
    },
    myStyles1() {
      return {
        height: `${this.height}%`,
        width: `${this.width}%`,
        position: "relative",
      };
    },
  },
};
</script>
