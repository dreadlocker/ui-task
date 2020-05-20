<template>
  <form
    action=""
    method="post"
    class="form"
    :class="classes"
  >
    <h1>{{header}}</h1>
    <input type="email" placeholder="Email">
    <BaseButton
      :text="buttonText"
    />
  </form>
</template>

<script>
import BaseButton from "./BaseButton.vue"
// DA VALIDIRAM S JS FORM INPUT-A
export default {
  name: 'BaseForm',
  components: {
    BaseButton
  },
  props: {
    header: {
      type: String,
      required:true
    },
    emailRegexp: {
      type: RegExp,
      required:true
    },
    buttonText: {
      type: String,
      required:true
    },
    classes: {
      type: String,
    },
  }
}
</script>
