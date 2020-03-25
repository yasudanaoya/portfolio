<template lang="pug">
  nuxt-link(
    :to="'/' + option.path"
  )
    .header-menu-option
      span {{ option.title }}
</template>

<script>
export default {
  props: {
    option: {
      type: Object,
      required: false,
      default: () => ({ count: 0 })
    }
  }
}
</script>

<style lang="scss" scoped>
span {
  &:hover {
    padding-bottom: 0.5vh;
    border-bottom: solid thin;
  }
}
</style>
