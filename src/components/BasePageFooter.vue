<template>
  <div>
    <div class="incons-holder d-flex mx-auto">
      <BaseIcon
        v-for="iconSrc in icons"
        :key="iconSrc"
        :iconSrc="iconSrc"
      />
    </div>

    <div class="footer-holder">
      <div class="footer-content-holder mx-auto">
        <div class="footer-links-holder mb-4 d-flex align-items-center">
          <u v-for="link in info.links" :key="link">
            <a class="footer-link font-weight-light">{{link}}</a>
          </u>
        </div>
        <p class="footer-info pb-4 font-weight-light">{{info.text}}</p>
      </div>
    </div>
  </div>
</template>

<script>
import BaseIcon from '@/components/BaseIcon.vue'

export default {
  name: 'BasePageFooter',
  components: {
    BaseIcon,
  },
  props: {
    info: {
      type: Object,
      required: true
    },
    icons: {
      type: Array,
      required: true
    },
  }
}
</script>
