<template>
  <form
    action=""
    method="post"
    class="form"
    :class="classes"
  >
    <h1>{{header}}</h1>
    <input type="email" placeholder="Email">
    <BaseButton />
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
    classes: {
      type: String,
    },
  },
  data() {
    return {
      form: {
        header: "Open an account and start trading online",
        emailRegexp: /asd/gi,
      },
    }
  },
  computed: {
    header() {
      return this.form.header
    },
  }
}
</script>
