<template lang="pug">
  .logo-frame
    nuxt-link(
      to="/"
    )
      Title
</template>

<script>
import Title from '../atoms/Title'
export default {
  components: {
    Title
  }
}
</script>

<style lang="scss" scoped>
.logo-frame {
  margin: auto;
  white-space: nowrap;
  text-decoration: none;
  a {
    text-decoration: none;
  }
}
</style>
