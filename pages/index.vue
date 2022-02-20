<template>
  <v-container>
    <v-row >
     <widget :option="Echart_config.chartType.pie.option"/>
     <widget :option="Echart_config.chartType.pie.option"/>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { mapState } from 'vuex';
import widget from '~/components/widget.vue'
export default {
  name: 'IndexPage',
  components: { widget },
  computed:{
    ...mapState(["Echart_config"])
  },
}
</script>
