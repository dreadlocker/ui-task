<template>
  <div>
    {{headerText}}
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
