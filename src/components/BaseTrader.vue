<template>
  <div
    :class="{'window-divider': index < lastIndex}"
    class="trader-holder"
  >
    <img :src="trader.image" alt="">
    <div>{{trader.header}}</div>
    <div>{{trader.info}}</div>
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
