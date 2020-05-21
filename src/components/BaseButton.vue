<template>
  <button
    @click.prevent="submit"
    type="submit"
    :class="classes"
    class="btn-lg btn-warning font-weight-bold"
  >{{text}}</button>
</template>

<script>
export default {
  name: 'BaseButton',
  props: {
    submit: {
      type: Function,
      required: true
    },
    classes: {
      type: String
    },
  },
  data() {
    return {
      text: "Invest $5 now",
    }
  },
}
</script>
