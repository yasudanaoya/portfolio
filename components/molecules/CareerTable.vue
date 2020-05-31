<template lang="pug">
  .career-table
    caption(
      style="width: 70vw"
    ) 職歴
      table
        tr(
          v-for="(item, index) in table"
          :key="index"
        )
          td
            span {{ item.date }}
          td
            span {{ item.event }}
          td(
            v-for="(item, index) in item.exec"
            :key="index"
          )
            span {{ item }}
</template>

<script>
export default {
  data() {
    return {
      table: [
        {
          date: '2017/04',
          event: '株式会社セラク入社',
          exec: ['インフラエンジニア']
        },
        {
          date: '2018/10',
          event: 'シアトルコンサルティング株式会社入社',
          exec: ['WEB エンジニア']
        }
      ]
    }
  }
}
</script>
