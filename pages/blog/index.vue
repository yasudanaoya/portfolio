<template lang="pug">
  .blog-top
    template(v-if="posts.lenght")
      .blog-item(
        v-for="(post, index) in posts"
        :key="post.id"
      )
        .blog-title
          a {{ post.fields.title }}

</template>

<script>
// import client from '~/plugins/contentful'

// export default {
//   async asyncData({ env }) {
//     let posts = []
//     await client.getEntries({
//       content_type: env.CTF_BLOG_POST_TYPE_ID,
//       order: '-fields.publishDate'
//     }).then(res => (posts = res.items)).catch(console.error)
//     return { posts }
//   }
// }
</script>
