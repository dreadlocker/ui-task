<template>
  <div
    :class="{'window-divider': index < lastIndex}"
    class="step-window-holder absolutely-centered"
  >
    <div class="step-window-number">{{windowNumber}}</div>
    <div class="step-window-info-holder">
      <h2 class="window-header">{{step[0]}}</h2>
      <h3 class="window-content">{{step[1]}}</h3>
    </div>
    <div v-if="index < lastIndex" class="divider-arrow">&#9698;</div>
  </div>
</template>

<script>
export default {
  name: 'BaseStep',
  props: {
    step: {
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
