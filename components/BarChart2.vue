<script>
import { Bar } from 'vue-chartjs'
export default {
  extends: Bar,
  data(){
    return {
        chartdata: {
            labels: ['1', '2', '3'],
            datasets: [
                {
                  label: ['Data One'],
                  backgroundColor: '#268bd2',
                  data: [40, 30, 20],
                  borderColor: "#fff",
                  borderWidth: 1
                },
                {
                  label: ['Data One'],
                  backgroundColor: 'black',
                  data: [60, 70, 80,],
                  borderColor: "#fff",
                  borderWidth: 1
                },
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
                  stacked: true ,
                  ticks:{
                    fontColor: "black",
                  }
                }
              ],
              yAxes: [
                {
                  stacked: true,
                  gridLines: {
                    zeroLineColor: 'rgba(130,130,130,1)'	,
                  },
                  ticks:{
                    max:100,
                    min:0,
                    stepSize:10,
                    fontColor: "black",
                  }
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
                text: 'Stacked Chart'
            },
        }
    }
  },
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>
