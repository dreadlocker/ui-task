<template>
  <div class="page-header d-flex justify-content-center align-items-center w-100">
    <h1 class="page-header-text">{{text}}</h1>
  </div>
</template>

<script>

export default {
  name: "BasePageHeader",
  props: {
    text: {
      type: String,
      required: true
    },
  },
};
</script>
