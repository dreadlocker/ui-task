<template>
  <form
    class="form d-flex flex-column justify-content-center mx-auto"
    :class="classes"
  >
    <div class="form-content-holder mx-auto">
      <h1 class="form-header text-center mx-auto">{{header}}</h1>
      <input
        @input="$emit('update', $event.target.value)"
        type="email"
        class="form-control"
        placeholder="Email"
        aria-label="Email"
        aria-describedby="basic-addon1"
      >
      <div
        v-if="isInputValid === false"
        class="p-1 mb-2 bg-danger text-white"
      >{{errorMessage}}</div>

      <BaseButton
        :onClick="submitForm"
        :type="'submit'"
        :text="buttonText"
      />
    </div>
  </form>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "BaseForm",
  components: {
    BaseButton
  },
  props: {
    header: {
      type: String,
      required: true
    },
    isInputValid: {
      type: [Boolean, String],
      required: true
    },
    errorMessage: {
      type: String,
      required: true
    },
    buttonText: {
      type: String,
      required: true
    },
    submitForm: {
      type: Function,
      required: true
    },
    classes: {
      type: String,
    },
  },
};
</script>
