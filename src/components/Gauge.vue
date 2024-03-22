<template>

  <div class="d-flex flex-column">
    <h2>Todays occupancy</h2>

    <div class="test position-relative ">

      <div class="position-absolute d-flex flex-column   w-100 h-100 justify-content-end align-items-center">
        <p class="mb-0">intitulé</p>
        <p class="mb-0">valeur gen</p>
      </div>

      <Doughnut :data="data" :options="options" />

    </div>
  </div>
</template>


<script >
import {Doughnut} from "vue-chartjs";

const data = {
  value: 200,
  max: 500,
  label: "Occupied rooms"
};

export default{
  name: 'gauge',
  components: {Doughnut},
  data(){
    return{
      data: {
        labels: [data.label],
        datasets: [{
          data: [data.value, data.max - data.value],
          backgroundColor: ['rgba(54, 162, 235, 0.8)', 'rgba(0, 0, 0, 0.1)'],
          borderWidth: 0
        }]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        cutoutPercentage: 100,
        rotation: -90,
        circumference: 180,
        tooltips: {
          enabled: false
        },
        legend: {
          display: false
        },
        animation: {
          animateRotate: true,
          animateScale: false
        },

      }
    };

  }
}

</script>



<style scoped>

</style>