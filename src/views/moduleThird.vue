<template>
  <div class="module-box" style="height: 35%">
    <div style="flex: 0 1 50%">
      <dv-border-box-8 style="width: 100%; height: 90%"
        ><chart
      /></dv-border-box-8>
    </div>
    <div style="flex: 0 1 25%">
      <dv-border-box-13 style="width: 100%; height: 90%"
        ><chartone
      /></dv-border-box-13>
    </div>
    <div style="flex: 0 1 25%">
      <dv-border-box-8 style="width: 100%; height: 90%"
        ><charttwo
      /></dv-border-box-8>
    </div>
  </div>
</template>

<script>
import chart from "./lineCharts.vue";
import chartone from "./lineChartsOne.vue";
import charttwo from "./lineChartsTwo.vue";

export default {
  components: {
    chart,
    chartone,
    charttwo,
  },
};
</script>

<style scoped>
::v-deep .border-box-content {
  display: flex !important;
  justify-content: center !important;
  align-items: center !important;
}
</style>
