<template>
  <form
    action=""
    method="post"
    class="form mx-auto w-100"
    :class="classes"
  >
    <h1 class="form-header text-center mx-auto">{{header}}</h1>
    <input type="email" class="form-control" placeholder="Email" aria-label="Email" aria-describedby="basic-addon1">
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
