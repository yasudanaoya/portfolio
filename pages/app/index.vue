<template lang="pug">
  .apps-top
    ul.app-list
      li
        a(
          href="http://atumori-kabuchart.com/"
        ) あつ森株価チャート
          img(
            :src="appImg"
          )
</template>

<script>
import appImg from '~/assets/images/chart.png'

export default {
  data() {
    return {
      appImg
    }
  }
}
</script>
