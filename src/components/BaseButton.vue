<template>
  <button type="submit">{{text}}</button>
</template>

<script>
export default {
  name: 'BaseButton',
  props: {
    text: {
      type: String,
      required: true
    }
  }
}
</script>
