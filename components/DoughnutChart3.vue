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
            data: [50, 60],
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
          text: "",
        },
      },
    };
  },
  mounted() {
    this.addPlugin({
      afterDraw(chart, go) {
        let ctx = chart.ctx
        chart.data.datasets.forEach((dataset, i) => {
        })

        // 中央にテキスト表示
        let fontSize = 10;
        let fontStyle = 'normal';
        let fontFamily = "Helvetica Neue";
        ctx.fillStyle = 'gray';
        ctx.font = Chart.helpers.fontString(fontSize, fontStyle, fontFamily);

        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';

        // position(第二, 第三引数は適宜調整)
        ctx.fillText('SPEED REAR', chart.width / 2 - 1, chart.height / 1.8);
      }
    })
    this.renderChart(this.chartdata, this.options);
  },
};
</script>
