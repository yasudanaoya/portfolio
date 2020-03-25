<template lang="pug">
  div.layout
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
.layout {
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  overflow: hidden;
  .default {
    margin: 2vh 15%;
    flex: 1;
  }
  .full-width {
    width: 100%;
  }
}
</style>
