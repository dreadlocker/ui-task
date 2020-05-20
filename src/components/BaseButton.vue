<template>
  <button
    type="submit"
    class="btn"
  >{{text}}</button>
</template>

<script>
export default {
  name: 'BaseButton',
  data() {
    return {
      text: "Invest $5 now",
    }
  }
}
</script>
