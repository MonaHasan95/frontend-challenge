<template>
  <section class="container">
    <div class="columns">
      <div class="column">
        <line-chart></line-chart>
      </div>
    </div>
  </section>
</template>

<script>
import LineChart from '@/components/LineChart'

export default {
  name: 'VueChartJS',
  components: {
    LineChart
  }
}
</script>
