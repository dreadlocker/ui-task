<template>
  <div id="app">
    <HomePage />
  </div>
</template>

<script>
import HomePage from "@/views/HomePage/HomePage.vue";

export default {
  name: "App",
  components: {
    HomePage
  }
};
</script>

<style lang="sass">
@import "@/assets/styles/main.sass"
</style>
