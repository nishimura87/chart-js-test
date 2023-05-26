<script>
import { Doughnut } from 'vue-chartjs'
export default {
  extends: Doughnut,
  name: 'chart',
  data(){
    return {
        chartdata: {
            datasets: [
                {
                label: ['Data One'],
                data: [40,60],
                backgroundColor: ['blue','transparent'],
                borderColor: "black",
                borderWidth: 1
                },
            ]
        },
        options: {
            responsive: true,
            cutoutPercentage : 90,
            maintainAspectRatio: false,
            legend: {
              display: false,
            },
            
        }
    }
  },
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>