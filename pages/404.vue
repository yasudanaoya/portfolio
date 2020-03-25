<template lang="pug">
  .error-image
    img(
      :src="image.notFound"
      alt="404 error"
    )
</template>

<script>
import NotFoundImage from '~/assets/images/404.png'

export default {
  data() {
    return {
      image: {
        notFound: NotFoundImage
      }
    }
  },
  head() {
    return {
      title: 'Not Found',
      titleTemplate: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.error-image {
  text-align: center;
  img {
    height: 60vh;
  }
}
</style>
