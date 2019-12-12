<script>
//  Importing Line class from the vue-chartjs wrapper
import { Line } from 'vue-chartjs'

//  Exporting this so it can be used in other components
export default {
  extends: Line,
  data() {
    return {
      datacollection: {
        //    Data to be represented on x-axis
        labels: ['13', '14', '15', '16', '17', '18', '19', '20'],
        datasets: [
          {
            label: 'Daily Activity Users',
            backgroundColor: '#29a79b',
            pointBackgroundColor: 'transparent',
            borderWidth: 1,
            pointBorderColor: 'transparent',
            //    Data to be represented on y-axis
            data: [249, 351, 973, 180, 666, 845, 455, 717]
          }
        ]
      },
      //  Chart.js options that controls the appearance of the chart
      options: {
        scales: {
          yAxes: [
            {
              ticks: {
                beginAtZero: true
              },
              gridLines: {
                display: false
              }
            }
          ],
          xAxes: [
            {
              gridLines: {
                display: false
              }
            }
          ]
        },
        legend: {
          display: true
        },
        labels: {
          display: false
        },
        responsive: true,
        maintainAspectRatio: true
      }
    }
  },
  mounted() {
    //    renderChart function renders the chart with the datacollection and options object.
    this.renderChart(this.datacollection, this.options)
  }
}
</script>
