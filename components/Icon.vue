<template>
  <img class="__icon" :src="url" alt="Icon">
</template>

<script>
const iconMap = {
  youtube: require('@/assets/images/icons/youtube.svg'),
  discord: require('@/assets/images/icons/discord.svg'),
  wechat: require('@/assets/images/icons/wechat.svg'),
  reddit: require('@/assets/images/icons/reddit.svg'),
  telegram: require('@/assets/images/icons/telegram.svg'),
  twitter: require('@/assets/images/icons/twitter.svg'),
  github: require('@/assets/images/icons/github.svg'),
  forum: require('@/assets/images/icons/forum.svg'),
  weibo: require('@/assets/images/icons/weibo.svg')
}

export default {
  props: {
    name: String
  },
  data () {
    return {
      iconMap
    }
  },
  computed: {
    url () {
      return this.iconMap[this.name]
    }
  }
}
</script>

<style lang="scss" scoped>
.__icon {
    width: 60px;
}
</style>
