<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col">
          <chart-card :chart-data="lineChart.data"
                      :chart-options="lineChart.options"
                      :responsive-options="lineChart.responsiveOptions">
            <template slot="header">
              <h4 class="card-title">Quick overview</h4>
              <p class="card-category">7 days</p>
            </template>
            <template slot="footer">
              <div class="legend">
                <i class="fa fa-circle text-info"></i> Mood
                <i class="fa fa-circle text-danger"></i> Sleep
                <i class="fa fa-circle text-warning"></i> Exercise
                <i class="fa fa-circle text-primary"></i> Option 3
              </div>
              <hr>
              <div class="stats">
                <i class="fa fa-history"></i> Updated 3 minutes ago
              </div>
            </template>
          </chart-card>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-md-3 col-md-offset-1">
          <button class="btn-outline-danger btn-block" @click="notifyVue('top', 'left')">Sleep</button>
        </div>
        <div class="col-md-3">
          <button class="btn-outline-warning btn-block" @click="notifyVue('top', 'left')">Exercise</button>
        </div>
        <div class="col-md-3">
          <button class="btn-outline-primary btn-block" @click="notifyVue('top', 'left')">Option 3</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import LTable from 'src/components/Table.vue'
  import Card from 'src/components/Cards/Card.vue'
  import ChartCard from 'src/components/Cards/ChartCard.vue'
  import StatsCard from 'src/components/Cards/StatsCard.vue'

  export default {
    components: {
      LTable,
      Card,
      ChartCard,
      StatsCard
    },

    data() {
      return {
        lineChart: {
          data: {
            labels: ['07/02', '08/02', '09/02', '10/02', '11/02', '12/02', '13/02'],
            series: [
              [20, 13, 21, 45, 45, 62, 21],
              [43, 54, 32, 45, 32, 45, 65],
              [12, 13, 14, 34, 45, 32, 9],
              [22, 43, 16, 54, 15, 52, 19]
            ]
          }
        }
      }
    },

    methods: {
    }
  }

</script>
<style lang="scss">

</style>
