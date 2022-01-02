<template>
  <div class="content">
    <div
      class="row"
      v-for="(val, i) in ['arr1', 'arr2', 'arr3', 'arr4', 'arr5']"
      :key="val"
      :style="{
        top: (initWidth / spacing) * i + 'px',
        left: (i & 1) === 0 ? 0 : initWidth / 2 + spacing + 'px'
      }"
    >
      <template v-for="n in 10">
        <Nest
          :key="n"
          :RADICAL_3="RADICAL_3"
          :spacing="spacing"
          :value="n + ''"
          color="#33b66e"
        ></Nest>
      </template>
    </div>
  </div>
</template>

<script>
import Nest from "./Nest.vue";
export default {
  data: function () {
    return {
      spacing: 3,
      RADICAL_3: 1.7320508,
      size: 80
    };
  },
  components: {
    Nest
  },
  computed: {
    initWidth() {
      return this.size || 80;
    }
  }
};
</script>

<style scoped>
  .content {
    padding: 50px;
  }
  .row {
    font-size: 0;
    position: relative;
  }
</style>
