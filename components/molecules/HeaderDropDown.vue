<template lang="pug">
  div
    .header-link
      span(
        @click="onClick"
      ) Portfolio
      drop-down-menu(
        v-if="dropDownOpen"
        @on-click="onClick"
      )
</template>

<script>
import DropDownMenu from './DropDownMenu'
export default {
  components: {
    DropDownMenu
  },
  data() {
    return {
      dropDownOpen: false
    }
  },
  methods: {
    onClick() {
      this.dropDownOpen = !this.dropDownOpen
    }
  }
}
</script>
