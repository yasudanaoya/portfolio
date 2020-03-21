<template lang="pug">
  .blog-card
    .blog-tags
      span {{ getPostTags }}
    .blog-img
      img(
        :src="post.image.fields.file.url"
        :alt="post.image.fields.title"
      )
    .blog-title
      span {{ post.title }}
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  },
  computed: {
    /**
     * tags が配列なので、文字列に変換して返却する
     */
    getPostTags() {
      return this.post.tags.join(',')
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
