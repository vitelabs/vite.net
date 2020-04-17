<template>
  <div>
    <div id="home" class="landing__home">
      <Nav />
      <b-container>
        <b-row class="__title__wrapper">
          <div class="mx-auto __title">
            Vite
          </div>
        </b-row>
        <b-row class="__title__wrapper">
          <div class="mx-auto __title_sub">
            {{ $t('slogan') }}
          </div>
        </b-row>
        <div class="__landing_img">
          <img src="@/assets/images/landing_vite@2x.png">
        </div>
      </b-container>
    </div>
    <div id="vitex" class="landing__section vitex">
      <b-container class="position-relative">
        <div class="text-center">
          <img class="mx-auto section__img img-fluid" src="@/assets/images/vitex@2x.png">
        </div>
        <b-row class="__section_content">
          <div class="__title mx-auto">
            {{ $t('vitex.title') }}
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto" v-html="$t('vitex.description')" />
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <a class="btn __button btn-secondary" :href="urls.vitex" target="_blank">{{ $t('vitex.useNow') }}</a>
            <a class="btn __button btn-secondary" :href="urls.vitexWebsite" target="_blank">{{ $t('vitex.learnMore') }}</a>
          </div>
        </b-row>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_app" class="landing__section vite_app">
      <b-container>
        <b-row>
          <b-col md="8" xs="12" sm="12" class="__section_content">
            <b-row>
              <div class="__title">
                {{ $t('app.title') }}
              </div>
            </b-row>
            <b-row class="__content" v-html="$t('app.description')" />
            <b-row class="__button_group">
              <a class="btn __button btn-secondary" :href="urls.ios" target="_blank">{{ $t('app.ios') }}</a>
              <a class="btn __button btn-secondary" :href="urls.android" target="_blank">{{ $t('app.android') }}</a>
              <a class="btn __button btn-secondary" :href="urls.appWebsite" target="_blank">{{ $t('app.learnMore') }}</a>
            </b-row>
          </b-col>
          <b-col md="auto" xs="12" sm="12" class="__section_img">
            <img class="img-fluid" src="@/assets/images/wallet@2x.png" alt="Vite Wallet">
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div id="vite_plus" class="landing__section vite_plus">
      <b-container class="position-relative">
        <b-row class="__section_content">
          <div class="__title mx-auto">
            {{ $t('vitePlus.title') }}
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto" v-html="$t('vitePlus.description')" />
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <a class="btn __button btn-secondary" :href="urls.vitePlus" target="_blank">{{ $t('vitePlus.learnMore') }}</a>
          </div>
        </b-row>
        <div class="text-center">
          <img class="mx-auto section__img img-fluid" src="@/assets/images/vite_plus@2x.png">
        </div>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_explorer" class="landing__section vite_explorer">
      <b-container>
        <b-row class="__section_content">
          <div class="__title mx-auto">
            {{ $t('explorer.title') }}
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto" v-html="$t('explorer.description')" />
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <b-button class="__button">
              <a :href="urls.viteScan" target="_blank">{{ $t('explorer.viteScan') }}</a>
            </b-button>
            <a class="btn __button btn-secondary" :href="urls.explorer" target="_blank">{{ $t('explorer.official') }}</a>
          </div>
        </b-row>
        <div class="text-center">
          <img class="mx-auto section__img img-fluid" src="@/assets/images/explorer@2x.png">
        </div>
      </b-container>
    </div>
    <div id="vite_web_wallet" class="landing__section vite_web_wallet">
      <b-container class="position-relative">
        <b-row class="__section_content">
          <div class="__title mx-auto">
            {{ $t('webWallet.title') }}
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto" v-html="$t('webWallet.description')" />
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <a class="btn __button btn-secondary" :href="urls.webWallet">{{ $t('webWallet.loginWebWallet') }}</a>
          </div>
        </b-row>
        <div class="text-center">
          <img class="mx-auto section__img img-fluid" src="@/assets/images/web_wallet@2x.png">
        </div>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_forum" class="landing__section vite_forum">
      <b-container class="position-relative">
        <b-row class="__section_content">
          <div class="__title mx-auto">
            {{ $t('forum.title') }}
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto" v-html="$t('forum.description')" />
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <a class="btn __button btn-secondary" :href="urls.forum" target="_blank">{{ $t('forum.toForum') }}</a>
          </div>
        </b-row>
        <div class="text-center">
          <img class="mx-auto section__img img-fluid" src="@/assets/images/forum@2x.png">
        </div>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue'

export default {
  components: { Nav },
  data () {
    return {
      urls: {
        vitex: 'https://x.vite.net/trade?symbol=VX_BTC-000',
        vitexWebsite: 'https://vitex.net',
        ios: 'https://apps.apple.com/us/app/vite-official-hd-wallet/id1437629486',
        android: 'https://play.google.com/store/apps/details?id=net.vite.wallet',
        appWebsite: 'https://app.vite.net/',
        vitePlus: 'https://donation.viteplus.net/',
        explorer: 'https://explorer.vite.net/',
        viteScan: 'https://vitescan.io/',
        webWallet: 'https://x.vite.net',
        forum: 'https://forum.vite.net'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~assets/css/vars.scss";

.landing__home {
  min-height: 500px;
  background-image: url("~assets/images/top_blue@2x.png");
  background-size: cover;
  background-position-y: bottom;
  text-align: center;

  .__title__wrapper {
    font-family: PingFangSC-Regular, PingFang SC;
    .__title {
      text-align: center;
      color: rgba(255, 255, 255, 1);
      font-size: 40px;
      font-weight: 600;
      margin-bottom: 50px;
      line-height: 70px;
      letter-spacing: 5px;
    }
    .__title_sub {
      font-size: 32px;
      font-weight: 400;
      line-height: 36px;
      letter-spacing: 3px;
      color: rgba(255, 255, 255, 1);
    }
  }
  .__landing_img {
    img {
      width: 100%;
    }
  }
  @include media-breakpoint-up(md) {
    min-height: 500px;
    .__title__wrapper {
      .__title {
        margin-top: 80px;
        font-size: 40px;
        font-weight: 600;
        margin-bottom: 50px;
        line-height: 70px;
        letter-spacing: 5px;
      }
      .__title_sub {
        font-size: 32px;
        font-weight: 400;
        line-height: 36px;
        letter-spacing: 3px;
      }
    }
  }
  @include media-breakpoint-up(lg) {
    min-height: 1025px;
    .__title__wrapper {
      .__title {
        margin-top: 80px;
        font-size: 40px;
        font-weight: 600;
        margin-bottom: 50px;
        line-height: 70px;
        letter-spacing: 5px;
      }
      .__title_sub {
        font-size: 32px;
        font-weight: 400;
        line-height: 36px;
        letter-spacing: 3px;
      }
    }
  }
  @include media-breakpoint-up(xl) {
    min-height: 1425px;
    .__title__wrapper {
      .__title {
        font-size: 50px;
        margin-top: 100px;
      }
      .__title_sub {
        font-size: 32px;
      }
    }
  }
}

.landing__section {
  .block_img {
    display: none;
    @include media-breakpoint-up(lg) {
      display: block;
      width: 96px;
      position: absolute;
      right: 0;
      bottom: 161px;
    }
  }
  .section__img {
    max-width: 100%;
    @include media-breakpoint-up(lg) {
      max-width: 700px;
    }
  }
  .__section_content {
    .__title, .__content {
      padding-left: 15px;
      padding-right: 15px;
      @include media-breakpoint-up(lg) {
        padding-left: 0;
        padding-right: 0;
      }
    }
  }
  .__button_group {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
    width: 100%;
    .__button {
      height: 54px;
      box-shadow: 0px 8px 34px 0px rgba(0, 122, 255, 0.2);
      border-radius: 5px;
      padding: 0 30px;
      background-color: #007aff;
      border: none;
      font-weight: 600;
      color: white;
      line-height: 54px;
    }
    @include media-breakpoint-up(md) {
      .__button {
        padding: 0 53px;
      }
    }
    @include media-breakpoint-up(lg) {
      width: 700px;
    }
  }
  &.vitex,
  &.vite_plus,
  &.vite_explorer,
  &.vite_web_wallet,
  &.vite_forum {
    .__section_content {
      .__title {
        font-size: 32px;
        line-height: 45px;
        margin-bottom: 40px;
        font-weight: 600;
        color: rgba(23, 28, 52, 1);
      }
      .__content {
        font-weight: 400;
        color: rgba(84, 86, 90, 1);
        text-align: center;
        font-size: 16px;
        line-height: 26px;
        margin-bottom: 50px;
      }
    }
  }

  &.vitex {
    .block_img {
      left: 0;
      bottom: 70px;
    }
    .section__img {
      margin-bottom: 120px;
      margin-top: -20px;
    }
  }
  &.vite_plus {
    padding-top: 150px;
    .__button_group {
      .__button {
        margin-right: 0;
      }
    }
    .section__img {
      margin-top: 120px;
    }
  }
  &.vite_explorer {
    background-image: url(~assets/images/center_blue@2x.png);
    background-size: cover;
    background-color: #007aff;
    padding-top: 30px;
    padding-bottom: 30px;
    .section__img {
      margin-top: 120px;
    }
    .__section_content {
      .__title, .__content {
        color: white;
      }
      .__button_group {
        .__button {
          background: rgba(255, 255, 255, 1);
          color: #007aff;
        }
      }
    }
    @include media-breakpoint-up(md) {
      padding-bottom: 296px;
      padding-top: 450px;
      background-color: transparent;
      margin-top: -230px;
    }
    @include media-breakpoint-up(lg) {
      padding-bottom: 296px;
      padding-top: 350px;
      background-color: transparent;
      margin-top: 0;
    }
  }
  &.vite_web_wallet {
    .block_img {
      left: 0;
    }
    .section__img {
      margin-top: 120px;
    }
    padding-top: 30px;
    @include media-breakpoint-up(md) {
      padding-top: 0;
    }
  }
  &.vite_forum {
    padding-top: 100px;
    padding-bottom: 30px;
    background-image: url("~assets/images/footer_blue@2x.png");
    background-size: cover;
    .__section_content {
      .__title {
        color: white;
      }
      .__content {
        color: white;
      }
      .__button {
        background: rgba(255, 255, 255, 1);
        color: #007aff;
      }
    }
    .section__img {
      margin-top: 120px;
    }
    @include media-breakpoint-up(md) {
      padding-top: 366px;
      padding-bottom: 150px;
    }
  }
  &.vite_app {
    background-color: #007aff;
    color: white;
    .__section_content {
      padding-top: 127px;
      padding-bottom: 127px;
      .__title {
        margin-bottom: 40px;
        font-size: 32px;
        font-weight: 600;
        color: rgba(255, 255, 255, 1);
        line-height: 45px;
      }
      .__content {
        margin-bottom: 50px;
      }
      .__button_group {
        justify-content: space-around;
        width: auto;
        .__button {
          background: rgba(255, 255, 255, 1);
          color: #007aff;
          margin-top: 15px;
        }
      }
    }
    .__section_img {
      img {
        width: 100%;
      }
    }
    margin-top: 30px;
    @include media-breakpoint-up(md) {
      margin-top: 50px;
      .__section_content {
        .__button_group {
          .__button {
            margin-top: 15px;
            margin-right: 20px;
          }
        }
      }
      .__section_img {
        width: 380px;
        img {
          margin-top: 120px;
        }
      }
    }
    @include media-breakpoint-up(lg) {
      margin-top: 150px;
      .__section_img {
        img {
          margin-top: -100px;
        }
      }
      .__section_content {
        .__button_group {
          justify-content: space-between;
        }
      }
    }
    @include media-breakpoint-up(xl) {
      margin-top: 340px;
      .__section_content {
        .__button_group {
          .__button {
            margin-top: 0;
            margin-right: 50px;
          }
        }
      }
      .__section_img {
        img {
          margin-top: -184px;
        }
      }
    }
  }
}
</style>
