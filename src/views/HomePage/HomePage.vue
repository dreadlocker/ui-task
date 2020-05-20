<template>
  <div>
    <BasePageHeader
      :headerText="headerText"
      :form="form"
      :buttonText="buttonText"
    />
    <HomePageContent
      :stepsHeader="stepsHeader"
      :tradersHeader="tradersHeader"
      :form="form"
      :buttonText="buttonText"
    />
    <BasePageFooter
      :footerInfo="footerInfo"
    />
  </div>
</template>

<script>
import BasePageHeader from '@/components/BasePageHeader.vue'
import HomePageContent from './HomePageContent.vue'
import BasePageFooter from '@/components/BasePageFooter.vue'

export default {
  name: 'HomePage',
  components: {
    BasePageHeader,
    HomePageContent,
    BasePageFooter,
  },
  data() {
    return {
      headerText: "random WxH",
      stepsHeader: "3 Easy steps to start trading online",
      tradersHeader: "See how our traders make more",
      form: {
        header: "Open an account and start trading online",
        emailRegexp: /asd/gi,
      },
      buttonText: "Invest $5 now",
      footerInfo: {
        links: ["Privacy Policy", "Contact Us", "Terms and Conditions"],
        text: "Disclaimer: Contract for differences traded on margin carry a high degree of risk. As such they may not be suitable for all investors. As it can result in loss of some or all invested capital, please seek independent advice and ensure you fully understand the risks associated with trading."
      }
    }
  }
}
</script>
