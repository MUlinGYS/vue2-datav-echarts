<template>
  <div ref="chart" style="width: 100%; height: 100%"></div>
</template>

<script>
import * as echarts from "echarts";
export default {
  data() {
    return {};
  },
  methods: {
    linCharts() {
      // 基于准备好的dom，初始化echarts实例
      var chartDom = this.$refs.chart;
      var myChart = echarts.init(chartDom);
      var option;

      option = {
        tooltip: {
          trigger: "item",
        },
        legend: {
          top: "5%",
          left: "center",
        },
        series: [
          {
            name: "Access From",
            type: "pie",
            radius: ["40%", "70%"],
            avoidLabelOverlap: false,
            itemStyle: {
              borderRadius: 10,
              borderColor: "#fff",
              borderWidth: 2,
            },
            label: {
              show: false,
              position: "center",
            },
            emphasis: {
              label: {
                show: true,
                fontSize: 40,
                fontWeight: "bold",
              },
            },
            labelLine: {
              show: false,
            },
            data: [
              { value: 1048, name: "Search Engine" },
              { value: 735, name: "Direct" },
              { value: 580, name: "Email" },
              { value: 484, name: "Union Ads" },
              { value: 300, name: "Video Ads" },
            ],
          },
        ],
      };

      option && myChart.setOption(option);
    },
  },
  mounted() {
    this.linCharts();
  },
};
</script>
