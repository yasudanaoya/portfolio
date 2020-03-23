<template lang="pug">
  .header
    logo.header-logo

    header-menu.header-menu
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
  padding-bottom: 4vh;
  .header-logo {
    margin-left: 15%;
  }
  .header-menu {
    margin-right: 15%;
  }
}
</style>
