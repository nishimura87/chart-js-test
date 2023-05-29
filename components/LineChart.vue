<script>
import { Line } from 'vue-chartjs'
export default {
  extends: Line,
  data() {
    return {
      chartData: {
        labels: ['1', '2', '3', '4', '5'],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [50, 30,-20, 0, 10],
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
          yAxes: [
            {
              ticks:{
              max:100,
              min:-100,
              stepSize:20,
              fontColor: "black",
              }
            }
          ],
        },
        title: {
          display: true,
          position: "top",
          fontSize: 14,
          fontColor: "black",
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