
<script>
import { Bar } from 'vue-chartjs'

export default {
  name:'Datagraphic',
  extends:Bar,

    props: {
    label:{
      type:String
    },
    chartData: {
      type: Array,
      default: null
    },
    options: {
      type: Object,
      default: null
    }
  },

  component:{
  },

  mounted () {
    this.renderChart(this.chartdata, this.options);
  },

}
</script>

<style lang="scss" scoped>

</style>