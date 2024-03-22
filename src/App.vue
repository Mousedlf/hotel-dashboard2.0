<template>

  <div class="row d-flex vh-100">
    <div class="col-3">
<singular-values/>
      <revenu-detail/>

    </div>

    <div class="col-9">
      <div class="">
      </div>

      <div class="d-flex ">

        <website-visitors/>

      </div>

      <div class="">
        <gauge/>

      </div>
    </div>

  </div>

</template>


<script lang="ts">
import {defineComponent} from "vue";
import WebsiteVisitors from "@/components/websiteVisitors.vue";
import Test from "@/components/singularValues.vue";
import SingularValues from "@/components/singularValues.vue";
import RevenuDetail from "@/components/revenuDetail.vue";
import Gauge from "@/components/Gauge.vue";

export default defineComponent({
  components: {Gauge, RevenuDetail, SingularValues, Test, WebsiteVisitors}
})
</script>


<style scoped>

</style>
