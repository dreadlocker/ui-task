<template>
  <div class="trader-holder window-divider">
    <img :src="trader.image" alt="">
    <div>{{trader.header}}</div>
    <div>{{trader.info}}</div>
  </div>
</template>

<script>
export default {
  name: 'HomePageTrader',
  props: {
    trader: {
      type: Object,
      required: true,
      validator: (arr) => Object.keys(arr).length === 3
    },
  },
}
</script>
