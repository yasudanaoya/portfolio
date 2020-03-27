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
