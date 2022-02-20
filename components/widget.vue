<template>
  <v-col cols="12" sm="4" style="background-color: white;">
    <v-chart class="chart" :option="option" />
  </v-col>
</template>

<script>
import { use } from "echarts/core";
import { CanvasRenderer } from "echarts/renderers";
import { PieChart } from "echarts/charts";
import {
  TitleComponent,
  TooltipComponent,
  LegendComponent
} from "echarts/components";
import VChart, { THEME_KEY } from "vue-echarts";

use([
  CanvasRenderer,
  PieChart,
  TitleComponent,
  TooltipComponent,
  LegendComponent
]);

export default {
  name: "HelloWorld",
  components: {
    VChart
  },
  provide: {
    [THEME_KEY]: ""
  },
  props:["option"],
};
</script>

<style scoped>
.chart {
  height: 300px;
}
</style>