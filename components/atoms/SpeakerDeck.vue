<template lang="pug">
  script(
    async
    class="speakerdeck-embed"
    :data-id="id"
    data-ratio="1.77777777777778"
    src="//speakerdeck.com/assets/embed.js"
  )
</template>

<script>
export default {
  props: {
    id: {
      type: Number,
      required: true
    }
  }
}
</script>
