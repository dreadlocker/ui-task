<template>
  <div>
    <div class="incons-holder content-holder mx-auto d-flex justify-content-between">
      <BaseIcon
        v-for="iconSrc in icons"
        :key="iconSrc"
        :iconSrc="iconSrc"
      />
    </div>

    <div class="footer-holder">
      <div class="footer-links-holder mb-4 d-flex flex-column align-items-center">
        <u
          v-for="link in footerInfo.links"
          :key="link"
        >
          <a
            href=""
            class="footer-link font-weight-light"
          >{{link}}</a>
        </u>
      </div>

      <p class="footer-info pb-4 font-weight-light">{{footerInfo.text}}</p>
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
  data() {
    return {
      footerInfo: {
        links: ["Privacy Policy", "Contact Us", "Terms and Conditions"],
        text: "Disclaimer: CFDs traded on margin carry a high degree of risk. As such they may not be suitable for all investors. As it can result in loss of some or all invested capital, please seek independent advice and ensure you fully understand the risks associated with trading."
      },
      icons: [
        require("@/assets/images/icon1.png"),
        require("@/assets/images/icon2.png"),
        require("@/assets/images/icon3.png"),
        require("@/assets/images/icon4.png"),
        require("@/assets/images/icon5.png"),
      ],
    }
  }
}
</script>
