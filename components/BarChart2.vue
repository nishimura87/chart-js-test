<script>
import { Bar } from 'vue-chartjs'
export default {
  extends: Bar,
  data(){
    return {
        chartdata: {
            labels: ['1', '2', '3', '4', '5'],
            datasets: [
                {
                  label: ['Data One'],
                  backgroundColor: '#f87979',
                  data: [40, 30, 20, 0, 10],
                  borderColor: "red",
                  borderWidth: 1
                },
                {
                  label: ['Data One'],
                  backgroundColor: 'transparent',
                  data: [60, 70, 80, 100, 90],
                  borderColor: "black",
                  borderWidth: 1
                },
            ]
        },
        options: {
            responsive: true,
            stacked: "100%",
            maintainAspectRatio: false,
            legend: {
              display: false,
            },
            scales: {
              xAxes: [
                {
                  stacked: true  // 積み上げの指定
                }
              ],
              yAxes: [
                {
                  stacked: true,
                  ticks:{
                    max:100,
                    min:0,
                    stepSize:10,
                    fontColor: "black",
                  }
                }
              ],
            }
        }
    }
  },
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>