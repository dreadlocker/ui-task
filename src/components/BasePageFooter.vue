<template>
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
</template>

<script>
export default {
  name: 'BasePageFooter',
  data() {
    return {
      footerInfo: {
        links: ["Privacy Policy", "Contact Us", "Terms and Conditions"],
        text: "Disclaimer: CFDs traded on margin carry a high degree of risk. As such they may not be suitable for all investors. As it can result in loss of some or all invested capital, please seek independent advice and ensure you fully understand the risks associated with trading."
      }
    }
  }
}
</script>
