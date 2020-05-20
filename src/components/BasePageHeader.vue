<template>
  <div class="page-header absolutely-centered">
    <h1 class="page-header-text">{{headerText}}</h1>
    
    <BaseForm
      :header="form.header"
      :emailRegexp="form.emailRegexp"
      :buttonText="buttonText"
      :classes="formClasses"
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
    formClasses: {
      type: String,
    },
  }
}
</script>
