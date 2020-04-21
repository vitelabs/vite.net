<template>
  <div class="footer">
    <b-container>
      <b-row>
        <b-col sm="12" xs="12" md="12" lg="4" class="logo">
          <img src="@/assets/images/logo@2x.png" class="logo__img" alt="Vite Logo">
        </b-col>
        <b-col sm="12" xs="12" lg="8" class="d-flex list__wrapper">
          <a v-for="item in urlList" :key="item.name" class="footer__navitem" :href="item.url"> {{ $t(`nav.${item.name}`) }} </a>
        </b-col>
      </b-row>
      <b-row>
        <b-col cols="12" class="footer__subtitle">
          {{ $t('footer.investor') }}
        </b-col>
        <b-col cols="12" class="list d-flex justify-content-start flex-wrap">
          <a v-for="item in investorList" :key="item.name" :href="item.url" target="_blank">
            <img class="footer__img" :src="`/images/investors/${item.name}@2x.png`" :alt="item.name">
          </a>
        </b-col>
        <b-col cols="12" class="footer__subtitle">
          {{ $t('footer.partner') }}
        </b-col>
        <b-col cols="12" class="list d-flex justify-content-start  flex-wrap">
          <a v-for="item in partnerList" :key="item.name" :href="item.url" target="_blank">
            <img class="footer__img" :src="`/images/partners/${item.name}@2x.png`" :alt="item.name">
          </a>
        </b-col>
        <b-col cols="12">
          <div class="footer__line" />
        </b-col>
        <b-col class="list d-flex justify-content-center justify-content-lg-between flex-wrap">
          <a v-for="item in iconUrlList" :id="`popover-${item.name}`" :key="item.name" :href="item.url">
            <icon :name="item.name" />
          </a>
        </b-col>
        <div>
          <b-popover target="popover-wechat" triggers="click" placement="top">
            <img style="width: 100%" src="@/assets/images/wxCode.png" alt="">
          </b-popover>
        </div>
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
        { name: 'weibo', url: 'https://weibo.com/u/6572727462' },
        { name: 'forum', url: 'https://forum.vite.net/' },
        { name: 'github', url: 'https://github.com/vitelabs' },
        { name: 'twitter', url: 'https://twitter.com/vitelabs' },
        { name: 'telegram', url: 'https://t.me/vite_ann' },
        { name: 'reddit', url: 'https://www.reddit.com/r/vitelabs/' },
        { name: 'wechat', url: 'javascript:void(0)' },
        { name: 'discord', url: 'https://discordapp.com/invite/CsVY76q' },
        { name: 'youtube', url: 'https://www.youtube.com/channel/UC8qft2rEzBnP9yJOGdsJBVg' },
        { name: 'medium', url: 'https://medium.com/vitelabs' },
        { name: 'facebook', url: 'https://www.facebook.com/vitelabs/' }
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
        { name: 'ok', url: 'https://www.okex.com/project/9' },
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
        { name: 'btc.com', url: 'https://btc.com/' },
        { name: 'ok', url: 'https://www.okex.com/' },
        { name: 'troy', url: 'https://troytrade.com/' },
        { name: 'f2pool', url: 'https://www.f2pool.com/' },
        { name: 'spark-pool', url: 'https://www.sparkpool.com/' },
        { name: 'harmony', url: 'https://harmony.one/' },
        { name: 'ankr', url: 'https://www.ankr.com/' },
        { name: 'hashfin', url: 'https://www.hashfin.com/zh-CN/' },
        { name: 'hash', url: 'https://www.hashquark.io/' },
        { name: 'vgate', url: 'https://vgate.io/' },
        { name: 'syra', url: 'http://www.syrgov.net/home.aspx' },
        { name: 'bi23', url: 'https://www.bi23.com/#/' },
        { name: 'xinsheng', url: '' },
        { name: 'vite-scan', url: 'https://vitescan.io/' },
        { name: 'knownsec', url: 'https://www.knownsec.com/#/' },
        { name: 'ACHpay', url: 'https://www.alchemytech.io/' }
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
    color: white;
    font-weight: 600;
    text-align: left;
    margin-top: 40px;
    @include media-breakpoint-up(md) {
      margin-top: 80px;
    }
  }
  .list__wrapper {
    flex-wrap: wrap;
    justify-content: center;
    .footer__navitem {
      padding-left: 15px;
      padding-right: 15px;
      color: white;
      font-size: 14px;
      line-height: 30px;
      font-weight: 600;
    }
    @include media-breakpoint-up(md) {
      padding-left: 15px;
      padding-right: 15px;
      .footer__navitem {
        color: white;
        font-size: 14px;
        line-height: 60px;
        font-weight: 600;
      }
    }
    @include media-breakpoint-up(lg) {
      justify-content: space-between;
      .footer__navitem {
        padding-right: 0;
        padding-left: 0;
      }
    }
  }
  .footer__img {
    width: 50px;
    height: 50px;
    margin-right: 16px;
    @include media-breakpoint-up(md) {
      width: 80px;
      height: 80px;
      margin-right: 44px;
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
