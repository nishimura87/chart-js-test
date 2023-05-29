<script>
import { HorizontalBarChart } from 'vue-chartjs';
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
  extends: HorizontalBarChart,
  data(){
    return {
        chartdata: {
            labels: ['1', '2', '3', '4', '5'],
            datasets: [
                {
                label: ['Data One'],
                backgroundColor: "#268bd2", // instead of this
                backgroundColor: pattern.draw("line-vertical", "#1f77b4"), // use this
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
        }
    }
  },
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>