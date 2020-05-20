<template>
  <img :src="iconSrc" alt="">
</template>

<script>
export default {
  name: 'BaseIcon',
  props: {
    iconSrc: {
      type: String,
      required: true
    }
  }
}
</script>
