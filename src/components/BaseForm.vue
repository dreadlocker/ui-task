<template>
  <form
    action=""
    method=""
    class="form mx-auto w-100"
    :class="classes"
  >
    <h1 class="form-header text-center mx-auto">{{header}}</h1>
    <input
      v-model="email"
      type="email"
      class="form-control"
      placeholder="Email"
      aria-label="Email"
      aria-describedby="basic-addon1"
    >
    <div
      v-if="isEmailWrong"
      class="p-1 mb-2 bg-danger text-white"
    >
      {{wrongEmailMessage}}
    </div>

    <BaseButton
      @checkEmail="checkEmail"
    />
  </form>
</template>

<script>
import BaseButton from "./BaseButton.vue"
// FIX REFACTOR CODE, ARRANGE CSS CLASSES IN MAIN.SASS, RUN ESLINT
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
        emailRegexp: /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/gi,
      },
      email: "",
      wrongEmailMessage: "Email you've entered is wrong.",
      isEmailWrong: false
    }
  },
  computed: {
    header() {
      return this.form.header
    },
  },
  methods: {
    checkEmail() {
      const isEmailCorrect = this.form.emailRegexp.test(this.email)
      if (isEmailCorrect) {
        this.isEmailWrong = false
        alert("Email is correct.")
      } else {
        this.isEmailWrong = true
      }
    }
  }
}
</script>
