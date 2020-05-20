<template>
  <div>
    <div>
      <span
        v-for="link in footerInfo.links"
        :key="link"
      >{{link}}</span>
    </div>

    <p>{{footerInfo.text}}</p>
  </div>
</template>

<script>
export default {
  name: 'BasePageFooter',
  props: {
    footerInfo: {
      type: Object,
      required: true
    }
  }
}
</script>
