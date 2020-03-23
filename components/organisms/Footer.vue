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
  bottom: 3%;
  height: 5vh;
  margin: 1vw 0;
  display: flex;
  padding: 4vh 0 2vh 0;
}
</style>
