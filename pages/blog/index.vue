<template lang="pug">
  .blog-top
    .blog-items
      blog-card(
        v-for="(content, index) in contents"
        :key="index"
        :index="index+1"
        :content="content.fields"
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
    let contents = []
    await client
      .getEntries({
        content_type: env.CTF_BLOG_POST_TYPE_ID,
        order: '-fields.publishedAt'
      })
      .then((res) => (contents = res.items))
    return { contents }
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
