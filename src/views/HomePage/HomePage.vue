<template>
  <div class="home-page-holder">
    <BasePageHeader :text="headerText" />
    <HomePageContent />
    <BaseForm
      :header="formHeader"
      :isInputValid="isInputValid"
      :errorMessage="formErrorMessage"
      :buttonText="buttonText"
      :submitForm="submitForm"
      @update="saveEmail"
    />
    <BasePageFooter
      :info="footerInfo"
      :icons="footerIcons"
    />
  </div>
</template>

<script>
import BasePageHeader from "@/components/BasePageHeader.vue";
import HomePageContent from "./HomePageContent.vue";
import BaseForm from "@/components/BaseForm.vue";
import BasePageFooter from "@/components/BasePageFooter.vue";

export default {
  name: "HomePage",
  components: {
    BasePageHeader,
    HomePageContent,
    BaseForm,
    BasePageFooter,
  },
  data() {
    return {
      headerText: "random WxH",
      formHeader: "Open an account and start trading online",
      isInputValid: "",
      formErrorMessage: "Email you've entered is wrong.",
      buttonText: "Invest $5 now",
      emailRegexp: /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/gi,
      enteredEmail: "",
      footerInfo: {
        links: ["Privacy Policy", "Contact Us", "Terms and Conditions"],
        text: "Disclaimer: CFDs traded on margin carry a high degree of risk. As such they may not be suitable for all investors. As it can result in loss of some or all invested capital, please seek independent advice and ensure you fully understand the risks associated with trading."
      },
      footerIcons: [
        require("@/assets/images/icon1.png"),
        require("@/assets/images/icon2.png"),
        require("@/assets/images/icon3.png"),
        require("@/assets/images/icon4.png"),
        require("@/assets/images/icon5.png"),
      ],
    };
  },
  methods: {
    saveEmail(val) {
      this.enteredEmail = val;
    },
    submitForm() {
      this.isInputValid = this.emailRegexp.test(this.enteredEmail);
      if (this.isInputValid) {
        alert("Thank you.");
      }
    }
  }
};
</script>
