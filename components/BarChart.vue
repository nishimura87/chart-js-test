<script>
import { Bar } from 'vue-chartjs';

export default {
  extends: Bar,
  data(){
    return {
        chartdata: {
            labels: ['1', '2', '3', '4', '5'],
            datasets: [
                {
                label: ['Data One'],
                backgroundColor: "#f87979",
                data: [40, 30,-20, 0, 10],
                }
            ]
        },

        options: {
            responsive: true,
            maintainAspectRatio: false,
            legend: {
              display: false,
            },
            title: {
                display: true,
                position: "top",
                fontSize: 14,
                fontColor: "black",
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