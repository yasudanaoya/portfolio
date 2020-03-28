<template lang="pug">
  .header
    .header-left
      logo

    .header-right
      .header-menu
        header-menu

        header-drop-down
</template>

<script>
import Logo from '../molecules/Logo'
import HeaderMenu from '../molecules/HeaderMenu'
import HeaderDropDown from '../molecules/HeaderDropDown'

export default {
  components: {
    Logo,
    HeaderMenu,
    HeaderDropDown
  }
}
</script>
