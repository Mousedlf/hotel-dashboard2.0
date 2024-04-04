<template>

  <div class="row d-flex vh-100">

    <div class="col-3">
      <singular-values/>
      <revenu-detail/>
      <gauge/>
    </div>

    <div class="col-9">
      <div class="">
        <revenu-gain-and-loss/>

      </div>

      <div class="d-flex ">
<!--        <gauge/>

        <website-visitors/>-->

      </div>

      <div class="d-flex">
     <!--   <revenu-detail/>

        <gauge/> -->

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
import RevenuGainAndLoss from "@/components/revenuGainAndLoss.vue";

export default defineComponent({
  components: {RevenuGainAndLoss, Gauge, RevenuDetail, SingularValues, Test, WebsiteVisitors}
})
</script>


<style scoped>

</style>
