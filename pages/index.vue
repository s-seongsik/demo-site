<template>
  <v-item-group>
    <v-container>
      <v-row>
        <v-col cols="12" md="4">
          <v-item >
            <v-card class="d-flex align-center" height="400">
              <widget :option="Echart_config.chartType.pie.option"/>
            </v-card>
          </v-item>
        </v-col>

        <v-col cols="12" md="8">
          <v-item >
            <v-card class="d-flex align-center" height="400">
              <widget :option="Echart_config.chartType.StackLine.option"/>
            </v-card>
          </v-item>
        </v-col>
      </v-row>
    </v-container>
  </v-item-group>
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
