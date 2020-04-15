<template>
  <div class="__footer_section">
    <b-container>
      <b-row>
        <b-col>
          <img src="@/assets/images/logo@2x.png" class="__logo" alt="Vite Logo">
        </b-col>
        <b-col>
          <a v-for="item in urlList" :key="item.name" :href="item.url">
            <icon :name="item.name" />
          </a>
        </b-col>
      </b-row>
      <b-row class="copy_right text-right">
        <b-col>
          © 2020 VITE Labs. All Rights Reserved.
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Icon from './Icon'

export default {
  components: { Icon },
  data () {
    return {
      urlList: [
        { name: 'weibo', url: '' },
        { name: 'forum', url: '' },
        { name: 'github', url: '' },
        { name: 'twitter', url: '' },
        { name: 'telegram', url: '' },
        { name: 'reddit', url: '' },
        { name: 'wechat', url: '' },
        { name: 'discord', url: '' },
        { name: 'youtube', url: '' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.__footer_section {
  padding-top: 35px;
  background-color: #006fe9;
  .__logo {
    width: 108px;
  }
  .copy_right {
    font-size: 12px;
    font-weight: 400;
    color: rgba(255, 255, 255, 1);
    line-height: 17px;
    padding-top: 30px;
    padding-bottom: 30px;
    text-align: center;
  }
}
</style>
