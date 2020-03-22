<template lang="pug">
  .footer
    footer-icons
</template>

<script>
import FooterIcons from '../molecules/FooterIcons'

export default {
  components: {
    FooterIcons
  }
}
</script>

<style lang="scss" scoped>
.footer {
  position: absolute;
  bottom: 3%;
  height: 5vh;
}
</style>
