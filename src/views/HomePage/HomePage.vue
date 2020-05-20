<template>
  <div class="home-page-holder">
    <BasePageHeader />
    <HomePageContent />
    <BaseForm />
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
}
</script>
