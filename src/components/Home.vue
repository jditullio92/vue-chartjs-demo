<template>
  <v-container>
    <v-row class="text-center">
      <v-col
        cols="12"
        md="6"
      >
        <v-card>
          <v-card-title>Total Responses by Member Code</v-card-title>
          <div class="pa-2">
            <BarChartDemo
              :chartData="chartData"
              :options="options"
            ></BarChartDemo>
          </div>
        </v-card>
      </v-col>
      <v-col
        cols="12"
        md="6"
      >
        <v-card>
          <v-card-title>Total Responses by Member Code</v-card-title>
          <div class="pa-2">
            <DoughnutChartDemo
              :chartData="chartData"
              :options="options"
            ></DoughnutChartDemo>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import BarChartDemo from './BarChartDemo';
import DoughnutChartDemo from './DoughnutChartDemo';
export default {
  components: {
    BarChartDemo,
    DoughnutChartDemo
  },
  data () {
    return {
      chartData: {
        labels: ['AREA01', 'ATT05', 'COR01', 'DOTA2'],
        datasets: [
          {
            backgroundColor: [
              '#41B883',
              '#E46651',
              '#00D8FF',
              '#DD1B16'
            ],
            data: [360, 190, 245, 420]
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false
      }
    }
  }
}
</script>
