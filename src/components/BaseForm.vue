<template>
  <form
    action=""
    method=""
    class="form d-flex flex-column justify-content-center mx-auto"
    :class="classes"
  >
    <div class="form-content-holder mx-auto">
      <h1 class="form-header text-center mx-auto">{{header}}</h1>
      <input
        v-model="enteredEmail"
        @input="sendEveryCharToParent()"
        type="email"
        class="form-control"
        placeholder="Email"
        aria-label="Email"
        aria-describedby="basic-addon1"
      >
      <div
        v-if="isEmailCorrect === false"
        class="p-1 mb-2 bg-danger text-white"
      >{{wrongEmailMessage}}</div>

      <BaseButton
        :onClick="submitForm"
        :type="'submit'"
        :text="buttonText"
      />
        <!-- @checkEmail="checkEmail" -->
    </div>
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
    isEmailCorrect: {
      type: [Boolean, String],
      required: true
    },
    submitForm: {
      type: Function,
      required: true
    },
    buttonText: {
      type: String,
      required: true
    },
    classes: {
      type: String,
    },
  },
  data() {
    return {
      header: "Open an account and start trading online",
      wrongEmailMessage: "Email you've entered is wrong.",
      enteredEmail: "",
    }
  },
  methods: {
    sendEveryCharToParent() {
      this.$emit('email', this.enteredEmail)
    }
  }
}
</script>
