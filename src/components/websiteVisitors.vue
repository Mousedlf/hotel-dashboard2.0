<template>
  <div class="d-flex flex-column">
    <h2>Website Visitors</h2>

    <div class="test position-relative ">

      <div class="position-absolute d-flex flex-column   w-100 h-100 justify-content-center align-items-center">
        <p class="mb-0">intitulé</p>
        <p class="mb-0">valeur gen</p>
      </div>

      <Doughnut :data="data" :options="options" />

    </div>
  </div>



</template>

<script lang="ts">
import {
  Chart as ChartJS,
  ArcElement, Title, Tooltip, Legend,
} from 'chart.js'
import { Doughnut } from 'vue-chartjs'

ChartJS.register(ArcElement, Title, Tooltip, ) //Legend

export default {
  name: 'websiteVisitors',
  components: {
    Doughnut
  },
  data() {
    return {
      data: {
        labels: ['Red', 'Blue', 'Yellow'],
        datasets: [{
          data: [300, 50, 100],
          backgroundColor: [
            'rgb(0,47,152)',
            'rgb(54, 162, 235)',
            'rgb(181,211,255)'
          ],
          hoverOffset: 4,

        }],

      },

      options: {
      //  responsive: true,
        pieceLabel: {
          render: 'label', //percentage
          precision: 2,
          position: 'outside',
          fontColor: '#000',
        }
      }
    }
  }
}
</script>

<style scoped>
.test{
  height: 33vh;
}

</style>