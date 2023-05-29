<script>
import { Line } from 'vue-chartjs'
export default {
  extends: Line,
  data() {
    return {
      chartData: {
        labels: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10'],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: 'rgba(130,130,130,0.3)',
            fill: true,
            borderColor: "#fff",
            lineTension: 0,
            borderWidth: 1,
            data: [0, 30, 80, 10, 10, 50, 30,-20, 0, 10],
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        legend: {
          display: false,
        },
        scales: {
          xAxes: [
            {
              ticks:{
                max:100,
                min:0,
                stepSize:5,
                fontColor: "black",
              },
            }
          ],
          yAxes: [
            {
              ticks:{
                fontColor: "black",
              },
              gridLines: {
                zeroLineColor: 'rgba(130,130,130,1)',
              },
            }
          ],
        },
        title: {
          display: true,
          position: "top",
          fontSize: 14,
          fontColor: "#fff",
          fontStyle: "bold",
          fontFamily: "sans-serif",
          text: 'Line Chart'
        },
      }
    }
  },
  mounted() {
    this.renderChart(this.chartData, this.options)
  },
}
</script>