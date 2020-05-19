<template>
  <div>
    <!-- <HomePageHeader
      :headerText="headerText"
    /> -->

    <div
      v-for="(content, index) in pageContent"
      :key="index"
    >
      <BaseHomePageContent
        :contentHeader="content.header"
        :contentWindows="content.windows"
      />
    </div>

    <!-- <HomePageFooter /> -->
  </div>
</template>

<script>
// import HomePageHeader from './HomePageHeader.vue'
import BaseHomePageContent from '@/components/BaseHomePageContent.vue'
// import HomePageFooter from './HomePageFooter.vue'

export default {
  name: 'HomePage',
  components: {
    // HomePageHeader,
    BaseHomePageContent,
    // HomePageFooter,
  },
  data() {
    return {
      headerText: "random WxH",
      // contentHeader1: "3 Easy steps to start trading online",
      pageContent: [
        {
          header: "3 Easy steps to start trading online",
          windows: [
            {
              header: "Fill your details",
              content: "Complete the registration form on this page ",
            },
            {
              header: "Deposit $5 to open an account",
              content: "Go to the platform, where you make a deposit.",
            },
            {
              header: "Make money",
              content: "Choose your assets, click BUY/SELL and make money",
            },
          ],
        },
        {
          header: "See how our traders make more",
          windows: [
            {
              header: "I started with $5, now I trade with over $1400 a week",
              content: "“The $5 investment is great because it gives you time to understand the platform and how trading works. I quickly upgraded to $200 and doubled my investment in no time.”",
            },
            {
              header: "This platfrom is a true revolution ",
              content: "“For me, trading is about mastering a skill and uBanker really helps you develop and improve as a trader. It’s a 5-star service!”",
            },
          ]
        }
      ],
      footerLinks: ["Privacy Policy", "Contact Us", "Terms and Conditions"],
      footerText: "Disclaimer: Contract for differences traded on margin carry a high degree of risk. As such they may not be suitable for all investors. As it can result in loss of some or all invested capital, please seek independent advice and ensure you fully understand the risks associated with trading."
    }
  }
}
</script>
