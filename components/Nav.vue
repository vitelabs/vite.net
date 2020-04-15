<template>
  <b-container class="__navbar_wrapper" fluid>
    <b-navbar class="__navbar" toggleable="lg" variant="faded">
      <b-navbar-brand href="#">
        <img class="__logo" src="~assets/images/logo@2x.png" alt="Vite Logo">
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse" />

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item v-for="link in links" :key="link.name" :href="link.url" right>
            {{ link.name }}
          </b-nav-item>
          <b-nav-item-dropdown class="__lang_select" text="选择语言" right>
            <b-dropdown-item href="#">
              EN
            </b-dropdown-item>
            <b-dropdown-item href="#">
              ES
            </b-dropdown-item>
            <b-dropdown-item href="#">
              RU
            </b-dropdown-item>
            <b-dropdown-item href="#">
              FA
            </b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      links: [
        { name: 'ViteX交易所', url: '#vitex' },
        { name: 'Vite APP', url: '#vite_app' },
        { name: 'Vite Plus', url: '#vite_plus' },
        { name: '区块浏览器', url: '#vite_explorer' },
        { name: '网页钱包', url: '#vite_web_wallet' },
        { name: '论坛', url: '#vite_forum' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~assets/css/vars.scss";

.__navbar_wrapper {
  @media (min-width: 1440px) {
    padding-right: 140px !important;
    padding-left: 140px !important;
  }
  .__navbar {
    .navbar-brand {
      .__logo {
        width: 108px;
      }
    }
    .navbar-toggler {
        border: none;
        .navbar-toggler-icon {
            color: white;
        }
    }
    .nav-link {
      color: white;
      font-size: 16px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      &:hover {
        color: white;
      }
      @include media-breakpoint-up(lg) {
          padding-left: 10px;
          padding-right: 10px;
      }
      @include media-breakpoint-up(xl) {
          padding-left: 20px;
          padding-right: 20px;
      }
      @media (min-width: 1440px) {
        padding-left: 30px;
        padding-right: 30px;
      }
    }
    .__lang_select {
      color: white;
      ::v-deep .nav-link {
        color: white !important;
      }
    }
  }
}
</style>
