<template>
  <form
    action=""
    method=""
    class="form d-flex flex-column justify-content-center mx-auto"
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
      v-if="isEmailCorrect === false"
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
      header: "Open an account and start trading online",
      emailRegexp: /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/gi,
      wrongEmailMessage: "Email you've entered is wrong.",
      email: "",
      isEmailCorrect: null
    }
  },
  methods: {
    checkEmail() {
      this.isEmailCorrect = this.emailRegexp.test(this.email)
      if (this.isEmailCorrect) {
        alert("Email is correct.")
      }
    }
  }
}
</script>
