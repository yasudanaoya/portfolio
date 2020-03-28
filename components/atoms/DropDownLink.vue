<template lang="pug">
  nuxt-link(
    :to="'/' + option.path"
  )
    .drop-down-link
      span(
        @click="onClick"
      ) {{ option.title }}
</template>

<script>
export default {
  props: {
    option: {
      type: Object,
      required: true
    }
  },
  methods: {
    onClick() {
      this.$emit('on-click')
    }
  }
}
</script>
