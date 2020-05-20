<template>
  <div class="home-page-header absolutely-centered">
    <h1 class="home-page-header-text">{{headerText}}</h1>
    
    <BaseForm
      :header="form.header"
      :emailRegexp="form.emailRegexp"
      :buttonText="buttonText"
    />
  </div>
</template>

<script>
import BaseForm from '@/components/BaseForm.vue'

export default {
  name: 'BasePageHeader',
  components: {
    BaseForm,
  },
  props: {
    headerText: {
      type: String,
      required: true
    },
    form: {
      type: Object,
      required: true
    },
    buttonText: {
      type: String,
      required: true
    },
  }
}
</script>
