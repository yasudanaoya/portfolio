<template lang="pug">
  .slide-top
    .slide-list
      .embed-slide(
          v-for="(embed, index) in embeds"
          :key="index"
        )
        speaker-deck(
          :id="embed.id"
        )
</template>

<script>
import SpeakerDeck from '../../components/atoms/SpeakerDeck'

export default {
  components: {
    SpeakerDeck
  },
  data() {
    return {
      embeds: [
        { id: '3458b05bc3774f58b3ef9f38e3441d62' },
        { id: 'c0d47535f53d4c80ae69ecde8fb4965c' },
        { id: '29a89b60233c4bfdba640bf24cd0f3ca' },
        { id: 'a68ef493957841459a1363c2471eed76' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.embed-slide {
  margin: 3vh 0;
  width: 100%;
}
</style>
