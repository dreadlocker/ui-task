<template>
  <button
    @click.prevent="onClick"
    :type="type"
    :class="classes"
    class="btn-lg btn-warning font-weight-bold"
  >{{text}}</button>
</template>

<script>
export default {
  name: 'BaseButton',
  props: {
    onClick: {
      type: Function,
      required: true
    },
    type: {
      type: String,
      required: true
    },
    text: {
      type: String,
      required: true
    },
    classes: {
      type: String
    },
  },
}
</script>
