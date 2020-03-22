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

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=M+PLUS+1p&display=swap');

span {
  font-family: 'M PLUS 1p', sans-serif;
  color: black;
}
.blog-card {
  float: left;
  margin: 2.5vh 2.5vw;
  width: 50%;
  border: 2px solid #000000;
  border-radius: 50px;
  .blog-tags {
    margin: 2vh 2vw;
    padding: 0 2vw;
    position: absolute;
    border: 2px solid black;
    border-radius: 50px;
  }
  .blog-img {
    text-align: center;
    img {
      height: 25vh;
      width: 100%;
      border-radius: 50px;
    }
  }
  .blog-title {
    margin: 5%;
  }
}
</style>
