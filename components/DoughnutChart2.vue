<script>
import { Doughnut } from "vue-chartjs";

export default {
  extends: Doughnut,
  name: "chart",
  data() {
    return {
      chartdata: {
        datasets: [
          {
            label: ["Data One"],
            data: [20, 50],
            backgroundColor: ["blue","purple"],
            borderWidth: 0,
          },
        ],
      },
      options: {
        responsive: true,
        cutoutPercentage: 90,
        rotation: -1.0 * Math.PI,
        circumference: Math.PI,
        maintainAspectRatio: false,
        legend: {
          display: false,
        },
        layout: {
          padding: {
            left: 5,
            right: 5,
          },
        },
        title: {
          display: true,
          position: "top",
          fontSize: 14,
          fontColor: "black",
          fontStyle: "bold",
          fontFamily: "sans-serif",
          text: "Doughnut Chart",
        },
      },
    };
  },
  mounted() {
    this.renderChart(this.chartdata, this.options);
  },
};
</script>
