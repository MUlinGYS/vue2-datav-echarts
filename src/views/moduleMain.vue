<template>
<div class="module-box" style="height:58%">
				<div style="flex: 0 1 25%">
					<dv-border-box-13 style="width: 100%; height: 33.33%" 
						><capsule :dataChart="dataChart" :colorsChart="colorsChart" style="padding:20px 10px 0 20px"/></dv-border-box-13>
						<dv-water-level-pond :config="config3" style="width: 100%; height: 33.33%;" />
					<dv-border-box-9 style="width: 100%; height: 33.33%"
						><dv-conical-column-chart :config="config5" style="width:90%;height:90%;margin-top:10px" /></dv-border-box-9
					>
				</div>
				<div style="flex: 0 1 50%">
					<dv-border-box-12 style="width: 100%; height: 100%"
						><dv-flyline-chart-enhanced :config="config4" style="width:100%;height:100%;" /></dv-border-box-12
					>
				</div>
				<div style="flex: 0 1 25%">
					<dv-border-box-1 style="width: 100%; height: 50%;"
						><dv-capsule-chart
							:config="config2"
							style="width: 90%; height: 90%;padding:20px 10px 0 20px" 
					/></dv-border-box-13></dv-border-box-1
					>
					<dv-border-box-8 style="width: 100%; height: 50%"
						><dv-scroll-ranking-board :config="config6" style="width:90%;height:100%" /></dv-border-box-8
					>
				</div>
			</div>
</template>
<script>
import capsule from './capsule.vue'

export default {
  name:'moduleMain',
  components: {
    capsule
  },
  data () {
    return {
      dataChart:[
        {
          name: "RO1",
          value: 1020,
        },        {
          name: "RO2",
          value: 1300,
        },        {
          name: "RO3",
          value: 2000,
        },        {
          name: "RO4",
          value: 1300,
        },        {
          name: "RO5",
          value: 1004,
        },        {
          name: "RO6",
          value: 1020,
        }
      ],
      colorsChart:["#e062ae", "#fb7293", "#e690d1", "#32c5e9", "#96bfff"],
      config2: {
        data: [
          {
            name: "南阳",
            value: 167,
          },
          {
            name: "周口",
            value: 123,
          },
          {
            name: "漯河",
            value: 98,
          },
          {
            name: "郑州",
            value: 75,
          },
          {
            name: "西峡",
            value: 66,
          },
        ],
        colors: ["#e062ae", "#fb7293", "#e690d1", "#32c5e9", "#96bfff"],
        unit: "单位",
        showValue: true,
      },
      config3: {
        data: [66],
        shape: "roundRect",
        waveOpacity: 0.2,
      },
      config4: {
        points: [
          {
            name: "郑州",
            coordinate: [0.48, 0.35],
            icon: {
              src: require("../assets/img/mapCenterPoint.png"),
              width: 30,
              height: 30,
            },
            halo: {
              show: true,
            },
          },
          {
            name: "新乡",
            coordinate: [0.52, 0.23],
          },
          {
            name: "焦作",
            coordinate: [0.43, 0.29],
          },
          {
            name: "开封",
            coordinate: [0.59, 0.35],
          },
          {
            name: "许昌",
            coordinate: [0.53, 0.47],
          },
          {
            name: "平顶山",
            coordinate: [0.45, 0.54],
          },
          {
            name: "洛阳",
            coordinate: [0.36, 0.38],
          },
          {
            name: "周口",
            coordinate: [0.62, 0.55],
          },
          {
            name: "漯河",
            coordinate: [0.56, 0.56],
          },
          {
            name: "南阳",
            coordinate: [0.37, 0.66],
          },
          {
            name: "信阳",
            coordinate: [0.55, 0.81],
          },
          {
            name: "驻马店",
            coordinate: [0.55, 0.67],
          },
          {
            name: "济源",
            coordinate: [0.37, 0.29],
          },
          {
            name: "三门峡",
            coordinate: [0.2, 0.36],
          },
          {
            name: "商丘",
            coordinate: [0.76, 0.41],
          },
          {
            name: "鹤壁",
            coordinate: [0.59, 0.18],
          },
          {
            name: "濮阳",
            coordinate: [0.68, 0.17],
          },
          {
            name: "安阳",
            coordinate: [0.59, 0.1],
          },
        ],
        lines: [
          {
            source: "新乡",
            target: "郑州",
          },
          {
            source: "焦作",
            target: "郑州",
          },
          {
            source: "开封",
            target: "郑州",
          },
          {
            source: "许昌",
            target: "郑州",
          },
          {
            source: "平顶山",
            target: "郑州",
          },
          {
            source: "洛阳",
            target: "郑州",
          },
          {
            source: "周口",
            target: "郑州",
          },
          {
            source: "漯河",
            target: "郑州",
          },
          {
            source: "南阳",
            target: "郑州",
          },
          {
            source: "信阳",
            target: "郑州",
          },
          {
            source: "驻马店",
            target: "郑州",
          },
          {
            source: "济源",
            target: "郑州",
          },
          {
            source: "三门峡",
            target: "郑州",
          },
          {
            source: "商丘",
            target: "郑州",
          },
          {
            source: "鹤壁",
            target: "郑州",
          },
          {
            source: "濮阳",
            target: "郑州",
          },
          {
            source: "安阳",
            target: "郑州",
          },
        ],
        bgImgSrc: require("../assets/img/map.jpg"),

        icon: {
          show: true,
          src: require("../assets/img/mapPoint.png"),
        },
      },
      config5:{
         data: [
    {
      name: '周口',
      value: 55
    },
    {
      name: '南阳',
      value: 120
    },
    {
      name: '西峡',
      value: 71
    },
    {
      name: '驻马店',
      value: 66
    },
    {
      name: '新乡',
      value: 80
    },
    {
      name: '信阳',
      value: 35
    },
    {
      name: '漯河',
      value: 15
    }
  ],
  img: [
    require('../assets/img/1st.png'),
    require('../assets/img//2st.png'),
    require('../assets/img//3st.png'),
    require('../assets/img//4st.png'),
    require('../assets/img//5st.png'),
    require('../assets/img//6st.png'),
    require('../assets/img//7st.png')
  ],
  showValue: true
      },
      config6:{
          data: [
    {
      name: '周口',
      value: 55
    },
    {
      name: '南阳',
      value: 120
    },
    {
      name: '西峡',
      value: 78
    },
    {
      name: '驻马店',
      value: 66
    },
    {
      name: '新乡',
      value: 80
    },
    {
      name: '信阳',
      value: 45
    },
    {
      name: '漯河',
      value: 29
    }
  ]
      }
  }
}
}
</script>

<style scoped>
::v-deep .border-box-content{
  display: flex !important;
  justify-content: center !important;
  align-content: center !important;
}
</style>
