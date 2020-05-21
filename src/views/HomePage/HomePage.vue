<template>
  <div class="home-page-holder">
    <BasePageHeader />
    <HomePageContent />
    <BaseForm
      :isInputValid="isInputValid"
      :submitForm="submitForm"
      :buttonText="buttonText"
      @update="saveEmail"
    />
    <BasePageFooter />
  </div>
</template>

<script>
import BasePageHeader from '@/components/BasePageHeader.vue'
import HomePageContent from './HomePageContent.vue'
import BaseForm from '@/components/BaseForm.vue'
import BasePageFooter from '@/components/BasePageFooter.vue'

export default {
  name: 'HomePage',
  components: {
    BasePageHeader,
    HomePageContent,
    BaseForm,
    BasePageFooter,
  },
  data() {
    return {
      isInputValid: "",
      emailRegexp: /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/gi,
      enteredEmail: "",
      buttonText: "Invest $5 now",
    }
  },
  methods: {
    saveEmail(val) {
      this.enteredEmail = val
    },
    submitForm() {
      this.isInputValid = this.emailRegexp.test(this.enteredEmail)
      if (this.isInputValid) {
        alert("Email is correct.")
      }
    }
  }
}
</script>
