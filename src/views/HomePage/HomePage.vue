<template>
  <div>
    <BasePageHeader
      :headerText="headerText"
      :form="form"
      :buttonText="buttonText"
      :formClasses="'header-form'"
    />
    <HomePageContent
      :stepsHeader="stepsHeader"
      :tradersHeader="tradersHeader"
      :form="form"
      :buttonText="buttonText"
    />
    <BasePageFooter />
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
    }
  }
}
</script>
