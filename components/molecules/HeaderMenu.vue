<template lang="pug">
  .header-menu
    header-menu-option(
      v-for="(option, index) in options"
      :key="index"
      :option="option"
    )
</template>

<script>
import HeaderMenuOption from '../atoms/HeaderMenuOption'

export default {
  components: {
    HeaderMenuOption
  },

  data() {
    return {
      options: [
        { title: 'blog', path: 'blog' },
        { title: 'Profile', path: 'profile' },
        { title: 'Home', path: '' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.header-menu {
  width: 100%;
}
</style>
