<template lang="pug">
  .blog-top
    template
      .blog-item(
        v-for="(post, index) in posts"
        :key="post.id"
      )
        .blog-title
          span {{ post.fields.title }}

</template>

<script>
import client from '~/plugins/contentful'

export default {
  async asyncData({ env }) {
    let posts = []
    await client
      .getEntries({
        content_type: env.CTF_BLOG_POST_TYPE_ID,
        order: '-fields.publishedAt'
      })
      .then((res) => (posts = res.items))
    return { posts }
  }
}
</script>
