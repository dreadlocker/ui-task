<template>
  <div>
    <div>
      <span
        v-for="link in footerInfo.links"
        :key="link"
      >{{link}}</span>
    </div>

    <p>{{footerInfo.text}}</p>
  </div>
</template>

<script>
export default {
  name: 'BasePageFooter',
  data() {
    return {
      footerInfo: {
        links: ["Privacy Policy", "Contact Us", "Terms and Conditions"],
        text: "Disclaimer: Contract for differences traded on margin carry a high degree of risk. As such they may not be suitable for all investors. As it can result in loss of some or all invested capital, please seek independent advice and ensure you fully understand the risks associated with trading."
      }
    }
  }
}
</script>
