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
