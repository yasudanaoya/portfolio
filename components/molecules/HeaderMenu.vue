<template lang="pug">
  div
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
        { title: 'Profile', path: 'profile' },
        { title: 'Home', path: '' }
      ]
    }
  }
}
</script>
