<template>
  <div>
    <HomePageHeader
      :headerText="headerText"
      class="home-page-header absolutely-centered"
    />
    <!-- <HomePageContent /> -->
    <!-- <HomePageFooter /> -->
  </div>
</template>

<script>
import HomePageHeader from './HomePageHeader.vue'
// import HomePageContent from './HomePageContent.vue'
// import HomePageFooter from './HomePageFooter.vue'

export default {
  name: 'HomePage',
  components: {
    HomePageHeader,
    // HomePageContent,
    // HomePageFooter,
  },
  data() {
    return {
      headerText: "random WxH",
      contentHeader1: "3 Easy steps to start trading online",
      content1Windows: [
        [
          "Fill your details",
          "Complete the registration form on this page ",
        ],
        [
          "Deposit $5 to open an account",
          "Go to the platform, where you make a deposit.",
        ],
        [
          "Make money",
          "Choose your assets, click BUY/SELL and make money",
        ],
      ],
      contentHeader2: "See how our traders make more",
      content2Windows: [
        [
          "I started with $5, now I trade with over $1400 a week",
          "“The $5 investment is great because it gives you time to understand the platform and how trading works. I quickly upgraded to $200 and doubled my investment in no time.”",
        ],
        [
          "This platfrom is a true revolution ",
          "“For me, trading is about mastering a skill and uBanker really helps you develop and improve as a trader. It’s a 5-star service!”",
        ],
      ],
      footerLinks: ["Privacy Policy", "Contact Us", "Terms and Conditions"],
      footerText: "Disclaimer: Contract for differences traded on margin carry a high degree of risk. As such they may not be suitable for all investors. As it can result in loss of some or all invested capital, please seek independent advice and ensure you fully understand the risks associated with trading."
    }
  }
}
</script>
