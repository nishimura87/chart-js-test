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
            data: [40, 30,-20, 0, 10],
          },
        ],
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        legend: {
              display: false,
            },
      },
    }
  },
  mounted() {
    this.renderChart(this.chartData, this.options)
  },
}
</script>