<script>
import { Doughnut } from 'vue-chartjs';
export default {
  extends: Doughnut,
  props: ['chartData', 'options'],
  mounted () {
    this.$nextTick(function () {
      this.renderChart(this.chartData, this.options);
    });
  }
}
</script>
