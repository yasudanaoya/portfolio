<template lang="pug">
  .footer-icons
    icon(
      v-for="(icon, index) in icons"
      :key="index"
      :icon="icon"
    )
</template>

<script>
import Icon from '../atoms/Icon'

// image
import TwitterIcon from '~/assets/images/icon/twitter.png'
import FacebookIcon from '~/assets/images/icon/facebook.png'
import GitHubIcon from '~/assets/images/icon/github.png'
import QiitaIcon from '~/assets/images/icon/qiita.png'

export default {
  components: {
    Icon
  },

  data() {
    return {
      icons: [
        {
          src: TwitterIcon,
          href: 'https://twitter.com/708yasuda',
          alt: 'Twitter'
        },
        {
          src: FacebookIcon,
          href: 'https://www.facebook.com/naoya.yasuda.50?ref=bookmarks',
          alt: 'Facebook'
        },
        {
          src: GitHubIcon,
          href: 'https://github.com/yasudanaoya',
          alt: 'GitHub'
        },
        {
          src: QiitaIcon,
          href: 'https://qiita.com/yasudanaoya',
          alt: 'Qiita'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.footer-icons {
  display: flex;
  right: 15%;
  position: absolute;
}
</style>
