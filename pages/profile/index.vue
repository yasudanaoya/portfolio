<template lang="pug">
  .profile-top
    career
</template>

<script>
import Career from '../../components/organisms/Career'

export default {
  components: {
    Career
  },
  head() {
    return {
      title: 'profile'
    }
  }
}
</script>
