<template>
  <div class="trader-holder d-flex flex-column window-divider">
    <img
      :src="trader.image"
      class="trader-image"
    >
    <h2 class="trader-header font-weight-bold mx-auto text-center">{{trader.header}}</h2>
    <h3 class="trader-quote font-weight-light mx-auto text-center">{{trader.info}}</h3>
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
