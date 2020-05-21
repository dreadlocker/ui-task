<template>
  <div class="trader-holder d-flex window-divider">
    <img
      :src="trader.image"
      class="trader-image"
      alt="trader"
    >
    <div class="trader-info-holder">
      <h2 class="trader-header font-weight-bold mx-auto">{{trader.header}}</h2>
      <h3 class="trader-quote font-weight-light mx-auto">{{trader.info}}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePageTrader',
  props: {
    trader: {
      type: Object,
      required: true,
      validator: (trader) => Object.keys(trader).length === 3
    },
  },
}
</script>
