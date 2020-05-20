<template>
  <div class="page-header d-flex justify-content-center align-items-center">
    <h1 class="page-header-text">{{headerText}}</h1>
    
    <BaseForm :classes="'hidden'" />
  </div>
</template>

<script>
import BaseForm from '@/components/BaseForm.vue'

export default {
  name: 'BasePageHeader',
  components: {
    BaseForm,
  },
  data() {
    return {
      headerText: "random WxH",
    }
  }
}
</script>
