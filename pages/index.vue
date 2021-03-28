<template>
  <div>
    <div id="home" class="landing">
      <Nav />
      <b-container>
        <b-row class="slogan">
          <div class="mx-auto slogan__title">
            Vite
          </div>
        </b-row>
        <b-row class="slogan">
          <div class="mx-auto slogan__title-sub">
            {{ $t('slogan') }}
          </div>
        </b-row>
        <div class="landing__img">
          <img src="@/assets/images/landing_vite@2x.png">
        </div>
      </b-container>
    </div>
    <div id="vitex" class="landing-section vitex">
      <b-container class="position-relative">
        <div class="text-center">
          <img class="mx-auto section__img img-fluid" :src="imgUrls.vitex">
        </div>
        <b-row class="section-content">
          <div class="section-content__title mx-auto">
            {{ $t('vitex.title') }}
          </div>
        </b-row>
        <b-row class="section-content">
          <div class="section-content__content mx-auto" v-html="$t('vitex.description')" />
        </b-row>
        <b-row class="section-content">
          <div class="mx-auto button-group">
            <a
              class="btn button-group__button btn-secondary"
              :href="urls.vitex"
              target="_blank"
            >{{ $t('vitex.useNow') }}</a>
            <a
              class="btn button-group__button btn-secondary"
              :href="urls.vitexWebsite"
              target="_blank"
            >{{ $t('vitex.learnMore') }}</a>
          </div>
        </b-row>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_app" class="landing-section vite_app">
      <b-container>
        <b-row>
          <b-col lg="8" xs="12" sm="12" class="section-content">
            <b-row>
              <div class="section-content__title">
                {{ $t('app.title') }}
              </div>
            </b-row>
            <b-row>
              <div class="section-content__content" v-html="$t('app.description')" />
            </b-row>
            <b-row class="button-group">
              <a
                class="btn button-group__button btn-secondary"
                :href="urls.ios"
                target="_blank"
              >{{ $t('app.ios') }}</a>
              <a
                class="btn button-group__button btn-secondary"
                :href="urls.android"
                target="_blank"
              >{{ $t('app.android') }}</a>
              <a
                id="popover-wallet-qr"
                class="btn button-group__button btn-secondary"
                href="javascript:void(0)"
              >
                {{ $t('app.qr') }}
                <b-popover target="popover-wallet-qr" triggers="hover" placement="top">
                  <img style="width: 100%" src="@/assets/images/qr-wallet.png" alt>
                </b-popover>
              </a>
              <a
                class="btn button-group__button btn-secondary"
                :href="urls.forumWallet"
                target="_blank"
              >{{ $t('app.learnMore') }}</a>
            </b-row>
          </b-col>
          <b-col lg="auto" xs="12" sm="12" class="__section_img">
            <img class="img-fluid" :src="imgUrls.wallet" alt="Vite Wallet">
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div id="vite_explorer" class="landing-section vite_explorer">
      <b-container>
        <b-row class="section-content">
          <div class="section-content__title mx-auto">
            {{ $t('explorer.title') }}
          </div>
        </b-row>
        <b-row class="section-content">
          <div class="section-content__content mx-auto" v-html="$t('explorer.description')" />
        </b-row>
        <b-row class="section-content">
          <div class="mx-auto button-group">
            <a
              class="btn button-group__button btn-secondary"
              :href="urls.viteScan"
              target="_blank"
            >{{ $t('explorer.viteScan') }}</a>
            <a
              class="btn button-group__button btn-secondary"
              :href="urls.explorer"
              target="_blank"
            >{{ $t('explorer.official') }}</a>
          </div>
        </b-row>
        <div class="text-center">
          <img class="mx-auto section__img_buttom img-fluid" :src="imgUrls.explorer">
        </div>
      </b-container>
    </div>
    <div id="vite_web_wallet" class="landing-section vite_web_wallet">
      <b-container class="position-relative">
        <b-row class="section-content">
          <div class="section-content__title mx-auto">
            {{ $t('webWallet.title') }}
          </div>
        </b-row>
        <b-row class="section-content">
          <div class="section-content__content mx-auto" v-html="$t('webWallet.description')" />
        </b-row>
        <b-row class="section-content">
          <div class="mx-auto button-group">
            <a
              class="btn button-group__button btn-secondary"
              :href="urls.webWallet"
            >{{ $t('webWallet.loginWebWallet') }}</a>
          </div>
        </b-row>
        <div class="text-center">
          <img
            class="mx-auto section__img_buttom img-fluid"
            :src="imgUrls.webWallet"
          >
        </div>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_forum" class="landing-section vite_forum">
      <b-container class="position-relative">
        <b-row class="section-content">
          <div class="section-content__title mx-auto">
            {{ $t('forum.title') }}
          </div>
        </b-row>
        <b-row class="section-content">
          <div class="section-content__content mx-auto" v-html="$t('forum.description')" />
        </b-row>
        <b-row class="section-content">
          <div class="mx-auto button-group">
            <a
              class="btn button-group__button btn-secondary"
              :href="urls.forum"
              target="_blank"
            >{{ $t('forum.toForum') }}</a>
          </div>
        </b-row>
        <div class="text-center">
          <img class="mx-auto section__img_buttom img-fluid" :src="imgUrls.forum">
        </div>
      </b-container>
    </div>
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue'

const imgUrlsMap = {
  zh: {
    vitex: require('@/assets/images/vitex@2x.png'),
    wallet: require('@/assets/images/wallet@2x.png'),
    vitePlus: require('@/assets/images/vite_plus@2x.png'),
    explorer: require('@/assets/images/explorer@2x.png'),
    webWallet: require('@/assets/images/web_wallet@2x.png'),
    forum: require('@/assets/images/forum@2x.png')
  },
  en: {
    vitex: require('@/assets/images/vitex_en@2x.png'),
    wallet: require('@/assets/images/wallet_en@2x.png'),
    vitePlus: require('@/assets/images/explorer_en@2x.png'),
    explorer: require('@/assets/images/explorer_en@2x.png'),
    webWallet: require('@/assets/images/web_wallet_en@2x.png'),
    forum: require('@/assets/images/forum@2x.png')
  }
}

export default {
  components: { Nav },
  data () {
    return {
      urls: {
        vitex: 'https://x.vite.net/trade?symbol=VX_BTC-000',
        vitexWebsite: 'https://vitex.net',
        ios:
          'https://apps.apple.com/us/app/vite-official-hd-wallet/id1437629486',
        android:
          'https://play.google.com/store/apps/details?id=net.vite.wallet',
        appWebsite: 'https://app.vite.net/',
        vitePlus: 'https://donation.viteplus.net/',
        explorer: 'https://explorer.vite.net/',
        viteScan: 'https://vitescan.io/',
        webWallet: 'https://x.vite.net',
        forum: 'https://forum.vite.net',
        forumWallet: 'https://forum.vite.net/category/36/vite-wallet'
      }
    }
  },
  computed: {
    imgUrls () {
      return imgUrlsMap[this.$i18n.locale] || imgUrlsMap.en
    }
  }
}
</script>

<style lang="scss">
@import "~assets/css/vars.scss";

.section-content__content {
  p {
    margin-bottom: 0;
  }
}
</style>

<style lang="scss" scoped>
@import "~assets/css/vars.scss";

.landing {
  min-height: 500px;
  background-image: url("~assets/images/top_blue@2x.png");
  background-size: cover;
  background-position-y: bottom;
  text-align: center;

  .slogan {
    font-family: PingFangSC-Regular, PingFang SC;
  }
  .slogan__title-sub {
    font-size: 25px;
    font-weight: 400;
    line-height: 36px;
    letter-spacing: 3px;
    color: rgba(255, 255, 255, 1);
  }
  .slogan__title {
    margin-top: 30px;
    text-align: center;
    color: rgba(255, 255, 255, 1);
    font-size: 30px;
    font-weight: 600;
    margin-bottom: 50px;
    line-height: 70px;
    letter-spacing: 5px;
  }
  .landing__img {
    img {
      width: 100%;
    }
  }
  @include media-breakpoint-up(md) {
    min-height: 500px;
    .slogan__title {
      margin-top: 80px;
      font-size: 40px;
      font-weight: 600;
      margin-bottom: 50px;
      line-height: 70px;
      letter-spacing: 5px;
    }
    .slogan__title-sub {
      font-size: 32px;
      font-weight: 400;
      line-height: 36px;
      letter-spacing: 3px;
    }
  }
  @include media-breakpoint-up(lg) {
    min-height: 1025px;
    .slogan__title {
      margin-top: 80px;
      font-size: 40px;
      font-weight: 600;
      margin-bottom: 50px;
      line-height: 70px;
      letter-spacing: 5px;
    }
    .slogan__title-sub {
      font-size: 32px;
      font-weight: 400;
      line-height: 36px;
      letter-spacing: 3px;
    }
  }
  @include media-breakpoint-up(xl) {
    min-height: 1425px;
    .slogan__title {
      font-size: 50px;
      margin-top: 100px;
    }
    .slogan__title-sub {
      font-size: 32px;
    }
  }
}

.landing-section {
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
  .section__img,
  .section__img_buttom {
    max-width: 100%;
    @include media-breakpoint-up(lg) {
      max-width: 700px;
    }
  }
  .section__img_buttom {
    margin-top: 60px;
    margin-bottom: 30px;
    @include media-breakpoint-up(md) {
      margin-top: 120px;
      margin-bottom: 0;
    }
  }
  .section-content__content {
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    line-height: 30px;
    color: rgba(84, 86, 90, 1);
    text-align: left;
    font-size: 14px;
    margin-bottom: 50px;
    @include media-breakpoint-up(md) {
      text-align: center;
    }
  }
  .section-content__title {
    font-size: 28px;
    line-height: 35px;
    margin-bottom: 30px;
    font-weight: 600;
    color: rgba(23, 28, 52, 1);
    @include media-breakpoint-up(md) {
      font-size: 32px;
      line-height: 45px;
      margin-bottom: 40px;
      font-weight: 600;
      color: rgba(23, 28, 52, 1);
    }
  }
  .section-content__title,
  .section-content__content {
    padding-left: 15px;
    padding-right: 15px;
    @include media-breakpoint-up(lg) {
      padding-left: 0;
      padding-right: 0;
    }
  }
  .button-group {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
    width: 100%;
    .button-group__button {
      height: 54px;
      box-shadow: 0px 8px 34px 0px rgba(0, 122, 255, 0.2);
      border-radius: 5px;
      padding: 0 30px;
      background-color: #007aff;
      border: none;
      font-weight: 600;
      color: white;
      line-height: 54px;
      width: 100%;
      margin-top: 15px;
      margin-right: 10px;
      margin-left: 10px;
      width: 100%;
    }
    @include media-breakpoint-up(md) {
      .button-group__button {
        padding: 0 53px;
        width: auto;
        margin-top: 0;
        margin-right: 0;
        margin-left: 0;
      }
    }
    @include media-breakpoint-up(lg) {
      width: 700px;
      justify-content: center;
      .button-group__button {
        margin-right: 50px;
        &:last-child {
          margin-right: 0;
        }
      }
    }
  }

  &.vitex {
    .block_img {
      left: 0;
      bottom: 70px;
    }
    .section__img {
      margin-bottom: 60px;
      margin-top: 30px;
    }
    @include media-breakpoint-up(md) {
      .section__img {
        margin-bottom: 120px;
        margin-top: -20px;
      }
    }
  }
  &.vite_plus {
    padding-top: 60px;
    @include media-breakpoint-up(md) {
      padding-top: 150px;
    }
  }
  &.vite_explorer {
    background-image: url(~assets/images/center_blue@2x.png);
    background-size: cover;
    background-color: #007aff;
    padding-top: 30px;
    padding-bottom: 30px;
    .section-content {
      .section-content__title,
      .section-content__content {
        color: white;
      }
      .button-group {
        .button-group__button {
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
    .section-content {
      .section-content__title {
        color: white;
      }
      .section-content__content {
        color: white;
      }
      .button-group__button {
        background: rgba(255, 255, 255, 1);
        color: #007aff;
      }
    }
    @include media-breakpoint-up(md) {
      padding-top: 366px;
      padding-bottom: 150px;
    }
  }
  &.vite_app {
    background-color: #007aff;
    .section-content {
      padding-top: 60px;
      padding-bottom: 60px;
      .section-content__title {
        color: rgba(255, 255, 255, 1);
      }
      .section-content__content {
        text-align: left;
        margin-bottom: 50px;
        color: white;
      }
    }
    .button-group {
      justify-content: space-around;
      width: auto;
      .button-group__button {
        background: rgba(255, 255, 255, 1);
        color: #007aff;
      }
    }
    .__section_img {
      margin-bottom: 30px;
      img {
        width: 100%;
      }
    }
    margin-top: 30px;
    @include media-breakpoint-up(md) {
      margin-top: 50px;
      .section-content {
        padding-top: 127px;
        padding-bottom: 127px;
      }
      .button-group {
        .button-group__button {
          margin-top: 15px;
          margin-right: 20px;
        }
      }
      .__section_img {
        margin-bottom: 0;
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
      .button-group {
        justify-content: space-between;
      }
    }
    @include media-breakpoint-up(xl) {
      margin-top: 340px;
      .__section_img {
        img {
          margin-top: -184px;
        }
      }
      .button-group {
        justify-content: start;
      }
    }
  }
}
</style>
