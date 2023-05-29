<script>
import {HorizontalBar} from 'vue-chartjs';
import pattern from "patternomaly";

const COLORS = [
  '#1f77b4',
  '#e377c2',
  '#ff7f0e',
  '#2ca02c',
  '#bcbd22',
  '#d62728',
  '#17becf',
  '#9467bd',
  '#7f7f7f',
  '#8c564b'
];

export default {
  extends: HorizontalBar,
  data(){
    return {
        chartdata: {
            labels: ['1', '2', '3'],
            datasets: [
                {
                label: ['Data One'],
                backgroundColor: [
                  pattern.draw("line-vertical", "#268bd2"),
                  pattern.draw("line-vertical", "#f87979"),
                  pattern.draw("line-vertical", "#268bd2"),
                ],
                data: [80, 80, 80],
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
                fontColor: "black",
                fontStyle: "bold",
                fontFamily: "sans-serif",
                text: 'Horizontal Bar Chart'
            },
        }
    }
  },
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>