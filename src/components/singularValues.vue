<script >
export default {
  data() {
    return {
      infos: [
          {
        title: 'graph 1',
        value: '393848'
      },
        {
          title: 'graph 2',
         value: '8393'
        },
        {
          title: 'graph 3',
          value: '5958'
        },
      ]
    }
  }
}

</script>

<template>
  <div v-for="info in infos">

    <h2>{{ info.title }}</h2>
    <div class="m-1 shadow d-flex justify-content-end bg-white py-2 mb-3">

          <p class="text-black pe-3 mb-0 fs-5">{{ info.value }}</p>

    </div>


  </div>

</template>

<style scoped>

</style>