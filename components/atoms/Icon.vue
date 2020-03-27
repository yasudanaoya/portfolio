<template lang="pug">
  .icon
    a(
      :href="icon.href"
      target="_blank"
    )
      img(
        :src="icon.src"
        :alt="icon.alt")
</template>

<script>
export default {
  props: {
    icon: {
      type: Object,
      required: true
    }
  }
}
</script>
