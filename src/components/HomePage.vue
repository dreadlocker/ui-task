<template>
  <div>
    <HomePageHeader />
    <HomePageContent />
    <HomePageFooter />
  </div>
</template>

<script>
import HomePageHeader from './HomePageHeader.vue'
import HomePageContent from './HomePageContent.vue'
import HomePageFooter from './HomePageFooter.vue'

export default {
  name: 'HomePage',
  components: {
    HomePageHeader,
    HomePageContent,
    HomePageFooter,
  },
}
</script>
