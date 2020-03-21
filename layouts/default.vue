<template lang="pug">
  div.default
    Header
    nuxt
</template>

<script>
import Header from '../components/organisms/Header'

export default {
  components: {
    Header
  }
}
</script>

<style lang="scss" scoped>
body {
  margin: 0;
  .default {
    margin: 2vh 15%;
  }
}
</style>
