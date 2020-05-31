<template lang="pug">
  .drop-down-menu
    drop-down-link(
      v-for="(option, index) in options"
      :key="index"
      :option="option"
      @on-click="onClick"
    )
</template>

<script>
import DropDownLink from '../atoms/DropDownLink'

export default {
  components: {
    DropDownLink
  },
  data() {
    return {
      options: [
        { title: 'Blog', path: 'blog' },
        { title: 'Slide', path: 'slide' },
        { title: 'Apps', path: 'app' }
      ]
    }
  },
  methods: {
    onClick() {
      this.$emit('on-click')
    }
  }
}
</script>
