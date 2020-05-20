<template>
  <div>
    <BasePageHeader />
    <HomePageContent />
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
}
</script>
