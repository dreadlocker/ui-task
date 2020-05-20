<template>
  <div>
    <div class="content-holder mx-auto">
      <div class="content-header d-flex align-items-center justify-content-center mx-auto font-weight-bold text-center">{{stepsHeader}}</div>
      <div class="windows-holder">
        <HomePageStep
          v-for="(step, index) in steps"
          :key="step[index]"
          :step="step"
          :windowNumber="index + 1"
        />
      </div>

      <div class="content-header d-flex align-items-center justify-content-center mx-auto font-weight-bold text-center">{{tradersHeader}}</div>
      <div class="windows-holder">
        <HomePageTrader
          v-for="(trader, index) in traders"
          :key="trader[index]"
          :trader="trader"
          :index="index"
        />
      </div>
    </div>
  </div>
</template>

<script>
import HomePageStep from './HomePageStep.vue'
import HomePageTrader from './HomePageTrader.vue'

export default {
  name: 'HomePageContent',
  components: {
    HomePageStep,
    HomePageTrader,
  },
  data() {
    return {
      stepsHeader: "3 Easy steps to start trading online",
      steps: [
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
      tradersHeader: "See how our traders make more",
      traders: [
        {
          image: require("@/assets/images/trader1.png"),
          header: "I started with $5, now I trade with over $1400 a week",
          info: "“The $5 investment is great because it gives you time to understand the platform and how trading works. I quickly upgraded to $200 and doubled my investment in no time.”",
        },
        {
          image: require("@/assets/images/trader2.png"),
          header: "This platfrom is a true revolution ",
          info: "“For me, trading is about mastering a skill and uBanker really helps you develop and improve as a trader. It’s a 5-star service!”",
        },
      ],
    }
  }
}
</script>
