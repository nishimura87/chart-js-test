<script>
import { Bar } from 'vue-chartjs';

export default {
  extends: Bar,
  data(){
    return {
        chartdata: {
            labels: ['1', '2', '3', '4', '5','6', '7', '8', '9', '10', '11', '12', '13', '14', '15','16', '17', '18', '19', '20'],
            datasets: [
                {
                label: ['Data One'],
                backgroundColor: "#fff",
                data: [70, 70, 70, 70, 60, 60, 70, -20, -20, -20, 70, 50, 50, 50, 50, 70, 70, 70, 50, 70],
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
                    fontColor: "black",
                  }
                }
              ],
              yAxes: [
                {
                  gridLines: {
                    zeroLineColor: 'rgba(130,130,130,1)',
                  },
                  ticks:{
                    fontColor: "black",
                  }
                }
              ]
            },
            title: {
                display: true,
                position: "top",
                fontSize: 14,
                fontColor: "#fff",
                fontStyle: "bold",
                fontFamily: "sans-serif",
                text: 'Bar Chart'
            },
        }
    }
  },
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>