<template>
  <button
    type="submit"
    :class="classes"
    class="btn-lg btn-warning w-100 font-weight-bold"
  >{{text}}</button>
</template>

<script>
export default {
  name: 'BaseButton',
  props: {
    classes: {
      type: String
    }
  },
  data() {
    return {
      text: "Invest $5 now",
    }
  }
}
</script>
