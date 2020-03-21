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
import { createClient } from '~/plugins/contentful.js'

const client = createClient()
export default {
  asyncData({ env, params }) {
    return client
      .getEntries(env.CTF_BLOG_POST_TYPE_ID)
      .then((entries) => {
        return {
          posts: entries.items
        }
      })
      .catch(console.error)
  }
}
</script>
