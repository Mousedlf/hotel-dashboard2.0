<template>

  <div class="row d-flex vh-100">
    <div class="col-3">
<singular-values/>

    </div>

    <div class="col-9">
      <div class="">
      </div>

      <div class="d-flex ">

        <website-visitors/>

      </div>

      <div class="">

      </div>
    </div>

  </div>

</template>


<script lang="ts">
import {defineComponent} from "vue";
import WebsiteVisitors from "@/components/websiteVisitors.vue";
import Test from "@/components/singularValues.vue";
import SingularValues from "@/components/singularValues.vue";

export default defineComponent({
  components: {SingularValues, Test, WebsiteVisitors}
})
</script>


<style scoped>

</style>
