<template lang="pug">
  div
    .header-link
      span(
        @mouseover="showMenu"
        @mouseleave="hideMenu"
      ) Portfolio
        drop-down-menu(
          v-show="dropDownOpen"
          @on-click="hideMenu"
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
    /**
     * ドロップダウンメニューを開く
     *
     * @returns {void}
     */
    showMenu() {
      this.dropDownOpen = true
    },
    /**
     * ドロップダウンメニューを閉じる
     *
     * @returns {void}
     */
    hideMenu() {
      this.dropDownOpen = false
    }
  }
}
</script>
