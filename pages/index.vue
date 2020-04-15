<template>
  <div>
    <div class="landing__home">
      <Nav />
      <b-container>
        <b-row class="__title__wrapper">
          <div class="mx-auto __title">
            Vite
          </div>
        </b-row>
        <b-row class="__title__wrapper">
          <div class="mx-auto __title_sub">
            全球首个基于DAG实现智能合约公链
          </div>
        </b-row>
        <b-row class="__landing_img">
          <img src="@/assets/images/landing_vite@2x.png">
        </b-row>
      </b-container>
    </div>
    <div id="vitex" class="landing__section vitex">
      <b-container class="position-relative">
        <b-row>
          <img class="mx-auto section__img img-fluid" src="@/assets/images/vitex@2x.png">
        </b-row>
        <b-row class="__section_content">
          <div class="__title mx-auto">
            完全去中心化交易所ViteX
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto">
            <p>全球首个基于DAG的完全去中心化交易所，无需KYC，保护个人信息；</p>
            <p>去中心化治理，交易、挂单、抵押、邀请、上币即挖矿，挖矿可得平台币VX，</p>
            <p>享受100%交易所手续费分红；社区自主上币，开交易所像开淘宝店一样简单</p>
            <p>助记词自己保管，资产更安全；链上撮合交易，秒级成交，接近中心化体验；支持跨链，可交易任何币种</p>
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <b-button class="__button">
              马上使用
            </b-button>
            <b-button class="__button">
              了解更多
            </b-button>
          </div>
        </b-row>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_app" class="landing__section vite_app">
      <b-container>
        <b-row>
          <b-col cols="8" class="__section_content">
            <b-row>
              <div class="__title">
                Vite APP
              </div>
            </b-row>
            <b-row class="__content">
              一款多币种开源手机钱包，只需一组助记词便可以管理多种加密资产
              内置去中心化交易所ViteX，交易、挖矿更便捷
              内置DApp丰富，投资娱乐两不误
              BTC.COM合作钱包，被鱼池、星火矿池、Luxor等矿池联袂推荐
            </b-row>
            <b-row class="__button_group">
              <b-button class="__button">
                iOS下载
              </b-button>
              <b-button class="__button">
                安卓下载
              </b-button>
              <b-button class="__button">
                了解更多
              </b-button>
            </b-row>
          </b-col>
          <b-col class="__section_img">
            <img class="img-fluid" src="@/assets/images/wallet@2x.png" alt="Vite Wallet">
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div id="vite_plus" class="landing__section vite_plus">
      <b-container class="position-relative">
        <b-row class="__section_content">
          <div class="__title mx-auto">
            VitePlus防疫物资溯源平台
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto">
            <p>基于Vite技术打造的VitePlus防疫物资溯源平台 ；实现捐赠信息链上全程溯源；从捐款者发布信息到物流运输等环节；所有数据保存在区块链；真实可信 公开透明且不可篡改</p>
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <b-button class="__button">
              了解更多
            </b-button>
          </div>
        </b-row>
        <b-row>
          <img class="mx-auto section__img img-fluid" src="@/assets/images/vite_plus@2x.png">
        </b-row>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_explorer" class="landing__section vite_explorer">
      <b-container>
        <b-row class="__section_content">
          <div class="__title mx-auto">
            区块浏览器
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto">
            <p>支持多币种钱包地址，交易，块高，哈希等信息的秒级查询；查询速度快，查询数据准确，功能完善的区块链浏览器</p>
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <b-button class="__button">
              官方开发
            </b-button>
            <b-button class="__button">
              社区开发
            </b-button>
          </div>
        </b-row>
        <b-row>
          <img class="mx-auto section__img img-fluid" src="@/assets/images/explorer@2x.png">
        </b-row>
      </b-container>
    </div>
    <div id="vite_web_wallet" class="landing__section vite_web_wallet">
      <b-container class="position-relative">
        <b-row class="__section_content">
          <div class="__title mx-auto">
            网络钱包
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto">
            <p>钱包与交易所一体化，在线交易、挖矿更方便</p>
            <p>多币种开源钱包，只需一组助记词便可以管理多种加密资产</p>
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <b-button class="__button">
              登录钱包
            </b-button>
          </div>
        </b-row>
        <b-row>
          <img class="mx-auto section__img img-fluid" src="@/assets/images/web_wallet@2x.png">
        </b-row>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
    <div id="vite_forum" class="landing__section vite_forum">
      <b-container class="position-relative">
        <b-row class="__section_content">
          <div class="__title mx-auto">
            Vite 论坛
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="__content mx-auto">
            <p>全球用户齐聚，第一时间了解Vite全部动态</p>
          </div>
        </b-row>
        <b-row class="__section_content">
          <div class="mx-auto __button_group">
            <b-button class="__button">
              前往论坛
            </b-button>
          </div>
        </b-row>
        <b-row>
          <img class="mx-auto section__img img-fluid" src="@/assets/images/forum@2x.png">
        </b-row>
        <img class="block_img" src="@/assets/images/block@2x.png" alt>
      </b-container>
    </div>
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue'

export default {
  components: { Nav }
}
</script>

<style lang="scss" scoped>
@import "~assets/css/vars.scss";

.landing__home {
  min-height: 1425px;
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
  .__button_group {
    .__button {
      height: 54px;
      box-shadow: 0px 8px 34px 0px rgba(0, 122, 255, 0.2);
      border-radius: 5px;
      padding: 0 53px;
      background-color: #007aff;
      border: none;
      font-weight: 600;
      &:first-child {
        margin-right: 50px;
      }
      &:last-child {
        margin-right: 0;
      }
    }
  }
  .section__img {
    max-width: 100%;
    @include media-breakpoint-up(lg) {
      max-width: 700px;
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
    padding-bottom: 296px;
    padding-top: 350px;
    .section__img {
      margin-top: 120px;
    }
    .__section_content {
      .__button_group {
        .__button {
          background: rgba(255, 255, 255, 1);
          color: #007aff;
        }
      }
    }
  }
  &.vite_web_wallet {
    .block_img {
      left: 0;
    }
    .section__img {
      margin-top: 120px;
    }
  }
  &.vite_forum {
    padding-top: 366px;
    padding-bottom: 150px;
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
  }
  &.vite_app {
    background-color: #007aff;
    color: white;
    .__section_content {
      padding-top: 127px;
      padding-bottom: 127px;
      padding-right: 95px;
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
        .__button {
          background: rgba(255, 255, 255, 1);
          color: #007aff;
        }
      }
    }
    .__section_img {
      width: 380px;
      img {
        width: 100%;
      }
    }
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
