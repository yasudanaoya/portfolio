<template lang="pug">
  .blog-card
    nuxt-link(
      :to="{name: 'blog-slug', params: { slug: content.slug }}"
    )
      .blog-tags(
        v-if="isHaveTags"
      )
        span {{ getContentTags }}
      .blog-img
        img(
          :src="content.image.fields.file.url"
          :alt="content.image.fields.title"
        )
      .blog-title
        span {{ content.title }}
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      required: true
    },
    index: {
      type: Number,
      required: true
    }
  },
  computed: {
    /**
     * タグを有するかのフラグ
     *
     * @return {boolean} 真偽値
     */
    isHaveTags() {
      return this.content.tags
    },
    /**
     * tags が配列なので、文字列に変換して返却する
     *
     * @return {string} タグ
     */
    getContentTags() {
      return this.content.tags.join(',')
    }
  }
}
</script>
