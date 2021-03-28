<template>
  <b-container class="__navbar_wrapper" fluid>
    <b-navbar class="__navbar" toggleable="lg" variant="faded">
      <b-navbar-brand href="#home">
        <img class="__logo" src="~assets/images/logo@2x.png" alt="Vite Logo">
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse" />

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item v-for="link in links" :key="link.name" :href="link.url" right>
            {{ $t(`nav.${link.name}`) }}
          </b-nav-item>
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
        { name: 'vitex', url: '#vitex' },
        { name: 'app', url: '#vite_app' },
        { name: 'vitePlus', url: '#vite_plus' },
        { name: 'explorer', url: '#vite_explorer' },
        { name: 'webWallet', url: '#vite_web_wallet' },
        { name: 'forum', url: '#vite_forum' }
      ]
    }
  },
  computed: {
    availableLocales () {
      return this.$i18n.locales.filter(i => i.code !== this.$i18n.locale)
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
