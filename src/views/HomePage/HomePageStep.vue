<template>
  <div class="step-holder d-flex window-divider position-relative">
    <div class="step-number d-flex align-items-center font-weight-bold">{{windowNumber}}</div>
    <div class="step-info-holder d-flex flex-column justify-content-center align-items-left">
      <h2 class="step-header font-weight-bold">{{step[0]}}</h2>
      <h3 class="step-content font-weight-light m-0">{{step[1]}}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePageStep',
  props: {
    step: {
      type: Array,
      required: true,
      validator: (step) => step.length === 2
    },
    windowNumber: {
      type: Number,
      required: true,
    },
  },
}
</script>
