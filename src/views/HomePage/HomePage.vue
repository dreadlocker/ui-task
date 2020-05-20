<template>
  <div>
    <BasePageHeader />
    <HomePageContent
      :stepsHeader="stepsHeader"
      :tradersHeader="tradersHeader"
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
      stepsHeader: "3 Easy steps to start trading online",
      tradersHeader: "See how our traders make more",
    }
  }
}
</script>
