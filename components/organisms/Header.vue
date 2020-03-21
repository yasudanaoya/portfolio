<template lang="pug">
  .header
    logo

    header-menu
</template>

<script>
import Logo from '../molecules/Logo'
import HeaderMenu from '../molecules/HeaderMenu'

export default {
  components: {
    Logo,
    HeaderMenu
  }
}
</script>

<style lang="scss" scoped>
.header {
  margin: 1vw 0;
  display: flex;
}
</style>
