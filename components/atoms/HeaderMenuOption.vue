<template lang="pug">
  nuxt-link(
    :to="'/' + option.path"
  )
    .header-menu-option
      span {{ option.title }}
</template>

<script>
export default {
  props: {
    option: {
      type: Object,
      required: false,
      default: () => ({ count: 0 })
    }
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=M+PLUS+1p&display=swap');

.header-menu-option {
  text-align: center;
  padding: 1vw;
  display: table-cell;
  vertical-align: middle;
  float: right;

  span {
    font-family: 'M PLUS 1p', sans-serif;
    color: black;
    &:hover {
      padding-bottom: 0.5vh;
      border-bottom: solid thin;
    }
  }
}
</style>
