<template>
  <div
    :class="{'window-divider': index < lastIndex}"
    class="trader-window-holder"
  >
    <img :src="trader.image" alt="">
    <div>{{trader.header}}</div>
    <div>{{trader.info}}</div>
    <!-- <div class="step-window-number">{{windowNumber}}</div>
    <div class="step-window-info-holder">
      <h2 class="window-header">{{trader[0]}}</h2>
      <h3 class="window-content">{{trader[1]}}</h3>
    </div>
    <div v-if="index < lastIndex" class="divider-arrow">&#9698;</div> -->
  </div>
</template>

<script>
export default {
  name: 'BaseTrader',
  props: {
    trader: {
      type: Object,
      required: true,
      validator: (arr) => Object.keys(arr).length === 3
    },
    index: {
      type: Number,
      required: true,
    },
    lastIndex: {
      type: Number,
      required: true,
    },
  },
  // computed: {
  //   windowNumber() {
  //     return this.index + 1
  //   }
  // },
}
</script>
