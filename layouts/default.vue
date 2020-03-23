<template lang="pug">
  div
    Header.full-width
    nuxt.default
    Footer.full-width
</template>

<script>
import Header from '../components/organisms/Header'
import Footer from '../components/organisms/Footer'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss" scoped>
body {
  margin: 0;
  .default {
    margin: 2vh 15%;
  }
  .full-width {
    width: 100%;
  }
}
</style>
