<template lang="pug">
  .icon
    a(
      :href="icon.href"
      target="_blank"
    )
      img(
        :src="icon.src"
        :alt="icon.alt")
</template>

<script>
export default {
  props: {
    icon: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
img {
  height: 5vh;
  margin: 0 0.5vw;
}
</style>
