<template>
  <button
    type="submit"
    :class="classes"
    class="btn"
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
