<template lang="pug">
  .blog-detail-top
    span {{ content.title }}
    .blog-body(
      v-html="$md.render(content.body)"
    )
</template>

<script>
import client from '~/plugins/contentful'
import Prism from '~/plugins/prism'

export default {
  async asyncData({ env, params }) {
    let content = null
    await client
      .getEntries({
        content_type: env.CTF_BLOG_POST_TYPE_ID,
        'fields.slug': params.slug
      })
      .then((res) => (content = res.items[0].fields))

    return { content }
  },
  mounted() {
    Prism.highlightAll()
  },
  head() {
    return {
      title: this.content.slug
    }
  }
}
</script>
