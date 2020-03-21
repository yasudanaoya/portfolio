<template lang="pug">
  .blog-top
    .blog-items
      blog-card(
        v-for="(post, index) in posts"
        :key="index"
        :post="post.fields"
      )
</template>

<script>
import client from '~/plugins/contentful'
import BlogCard from '~/components/organisms/BlogCard'

export default {
  components: {
    BlogCard
  },
  async asyncData({ env }) {
    let posts = []
    await client
      .getEntries({
        content_type: env.CTF_BLOG_POST_TYPE_ID,
        order: '-fields.publishedAt'
      })
      .then((res) => (posts = res.items))
    return { posts }
  },
  head() {
    return {
      title: 'blog'
    }
  }
}
</script>

<style lang="scss" scoped>
.blog-items {
  display: flex;
}
</style>
