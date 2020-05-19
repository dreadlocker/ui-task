<template>
  <div
    :class="{'content-window-holder-divider': index < lastIndex}"
    class="content-window-holder absolutely-centered"
  >
    <div class="content-window-number">{{windowNumber}}</div>
    <div class="content-window-info-holder">
      <h2 class="window-header">{{window[0]}}</h2>
      <h3 class="window-content">{{window[1]}}</h3>
    </div>
    <div v-if="index < lastIndex" class="window-content-divider">&#9698;</div>
  </div>
</template>

<script>
export default {
  name: 'BaseContentWindow',
  props: {
    window: {
      type: Array,
      required: true,
      validator: (arr) => arr.length === 2
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
  computed: {
    windowNumber() {
      return this.index + 1
    }
  },
}
</script>
