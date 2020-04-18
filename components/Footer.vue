<template>
  <div class="footer">
    <b-container>
      <b-row>
        <b-col sm="12" xs="12" md="12" lg="4" class="logo">
          <img src="@/assets/images/logo@2x.png" class="logo__img" alt="Vite Logo">
        </b-col>
        <b-col sm="12" xs="12" lg="8" class="d-flex justify-content-between">
          <a v-for="item in urlList" :key="item.name" class="footer__navitem" :href="item.url"> {{ $t(`nav.${item.name}`) }} </a>
        </b-col>
      </b-row>
      <b-row>
        <b-col cols="12" class="footer__subtitle">
          {{ $t('footer.investor') }}
        </b-col>
        <b-col cols="12" class="list d-flex justify-content-center flex-wrap">
          <a v-for="item in investorList" :key="item.name" :href="item.url" target="_blank">
            <img class="footer__img" :src="`/images/investors/${item.name}@2x.png`" :alt="item.name">
          </a>
        </b-col>
        <b-col cols="12" class="footer__subtitle">
          {{ $t('footer.partner') }}
        </b-col>
        <b-col cols="12" class="list d-flex justify-content-center flex-wrap">
          <a v-for="item in partnerList" :key="item.name" :href="item.url" target="_blank">
            <img class="footer__img" :src="`/images/partners/${item.name}@2x.png`" :alt="item.name">
          </a>
        </b-col>
        <b-col cols="12">
          <div class="footer__line" />
        </b-col>
        <b-col class="list d-flex justify-content-center justify-content-lg-between flex-wrap">
          <a v-for="item in iconUrlList" :key="item.name" :href="item.url">
            <icon :name="item.name" />
          </a>
        </b-col>
      </b-row>
      <b-row class="copy-right">
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
      iconUrlList: [
        { name: 'weibo', url: '' },
        { name: 'forum', url: '' },
        { name: 'github', url: '' },
        { name: 'twitter', url: '' },
        { name: 'telegram', url: '' },
        { name: 'reddit', url: '' },
        { name: 'wechat', url: '' },
        { name: 'discord', url: '' },
        { name: 'youtube', url: '' },
        { name: 'medium', url: '' },
        { name: 'facebook', url: '' }
      ],
      urlList: [
        { name: 'vitex', url: '#vitex' },
        { name: 'app', url: '#vite_app' },
        { name: 'vitePlus', url: '#vite_plus' },
        { name: 'explorer', url: '#vite_explorer' },
        { name: 'webWallet', url: '#vite_web_wallet' },
        { name: 'forum', url: '#vite_forum' }
      ],
      investorList: [
        { name: 'bitmain', url: 'https://www.bitmain.com/' },
        { name: 'ld', url: 'https://ldcap.com/' },
        { name: 'node', url: 'http://www.nodecap.com/' },
        { name: 'linkvc', url: 'http://www.linkvc.com/' },
        { name: 'funcity', url: 'http://www.funcityholding.com/' },
        { name: 'kosmos', url: 'http://kosmos.capital/' },
        { name: 'genesis', url: 'http://www.newgenesiscap.com/' },
        { name: 'byzantine', url: 'http://byzantinepartners.com/' },
        { name: 'distributed', url: 'http://distributed.fund/' },
        { name: 'bigcoin', url: 'https://www.linkedin.com/company/bigcoin-capital/' },
        { name: 'wandarin', url: 'http://wandarin.org/' },
        { name: 'starwin', url: 'https://www.tianyancha.com/organize/b5dfe14738' },
        { name: 'zhizi', url: '' },
        { name: 'hot', url: '' },
        { name: 'dazhi', url: '' },
        { name: 'uva', url: '' },
        { name: 'axi', url: '' },
        { name: 'handsome', url: '' },
        { name: 'hesheng', url: '' },
        { name: 'b100', url: '' },
        { name: 'bn', url: '' }
      ],
      partnerList: [
        { name: 'btc.com', url: '' },
        { name: 'troy', url: '' },
        { name: 'f2pool', url: '' },
        { name: 'spark-pool', url: '' },
        { name: 'harmony', url: '' },
        { name: 'ankr', url: '' },
        { name: 'hashfin', url: '' },
        { name: 'vgate', url: '' },
        { name: 'syra', url: '' },
        { name: 'bi23', url: '' },
        { name: 'xinsheng', url: '' },
        { name: 'vite-scan', url: '' },
        { name: 'knownsec', url: '' },
        { name: 'ACHpay', url: '' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~assets/css/vars.scss";

.footer {
  padding-top: 35px;
  background-color: #006fe9;
  .logo {
    text-align: center;
    margin-bottom: 30px;
    @include media-breakpoint-up(lg) {
      text-align: left;
      margin-bottom: 0;
    }
  }
  .footer__subtitle {
    font-size: 14px;
    margin-bottom: 10px;
    margin-top: 24px;
    color: white;
    font-weight: 600;
    &:first-child {
      margin-top: 80px;
    }
  }
  .footer__navitem {
    color: white;
    font-size: 14px;
    line-height: 60px;
    font-weight: 600;
  }
  .footer__img {
    width: 50px;
    height: 50px;
    margin-right: 8px;
    margin-left: 8px;
    @include media-breakpoint-up(md) {
      width: 80px;
      height: 80px;
      margin-right: 22px;
      margin-left: 22px;
    }
  }
  .logo__img {
    width: 108px;
  }
  .footer__line {
    height: 1px;
    width: auto;
    background-color: rgba(255,255,255,0.3);
    margin-bottom: 50px;
    margin-top: 50px;
  }
  .copy-right {
    font-size: 12px;
    font-weight: 400;
    color: rgba(255, 255, 255, 1);
    line-height: 17px;
    padding-top: 30px;
    padding-bottom: 30px;
    text-align: center;
    @include media-breakpoint-up(md) {
      text-align: right;
    }
  }
  .list {
    margin-top: 20px;
    @include media-breakpoint-up(md) {
      margin-top: 0;
    }
  }
  ::v-deep .__icon {
    width: 40px;
    @include media-breakpoint-up(md) {
      width: 60px;
    }
  }
}
</style>
