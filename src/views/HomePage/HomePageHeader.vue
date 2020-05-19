<template>
  <div class="home-page-header absolutely-centered">
    <h1 class="home-page-header-text">{{headerText}}</h1>
  </div>
</template>

<script>
export default {
  name: 'HomePageHeader',
  props: {
    headerText: {
      type: String,
      required: true
    }
  }
}
</script>
