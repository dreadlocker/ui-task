<template>
  <div
    :class="{'window-divider': index < lastIndex}"
    class="step-holder d-flex"
  >
    <div class="step-number d-flex align-items-center font-weight-bold">{{windowNumber}}</div>
    <div class="step-info-holder d-flex flex-column justify-content-center align-items-left">
      <h2 class="step-header font-weight-bold">{{step[0]}}</h2>
      <h3 class="step-content font-weight-light m-0">{{step[1]}}</h3>
    </div>
    <div v-if="index < lastIndex" class="divider-arrow position-absolute ">&#9698;</div>
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
