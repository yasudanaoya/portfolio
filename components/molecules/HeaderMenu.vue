<template lang="pug">
  .header-menu
    .header-link(
      v-for="(option, index) in options"
      :key="index"
    )
      header-menu-option(
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
        { title: 'Slide', path: 'slide' },
        { title: 'Blog', path: 'blog' },
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
  .header-link {
    text-align: center;
    padding: 1vw;
    display: table-cell;
    vertical-align: middle;
    float: right;
  }
}
</style>
