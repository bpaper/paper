<template>
  <div class="waring">
    <p class="title">当日天气</p>

    <mu-row class="weather">
      <mu-alert color="success" class="item">
        <mu-icon class="icon"> </mu-icon>
      </mu-alert>
      <mu-alert color="warning"> this is warning alert </mu-alert>
      <mu-alert color="info"> this is info alert </mu-alert>
      <mu-alert color="error"> this is error alert </mu-alert>
    </mu-row>

    <p class="title">安全手册</p>
    <mu-carousel transition="fade" interval="3000" class="carousel">
      <mu-icon value="navigate_before" slot="left"></mu-icon>
      <mu-icon value="navigate_next" slot="right"></mu-icon>

      <template slot="indicator" slot-scope="{ index, active }">
        <mu-button
          icon
          class="mu-carousel-indicator-button"
          :class="{ 'mu-carousel-indicator-button__active': active }"
          @click="changeActive(index)"
        >
          <span class="rect-indicator"></span>
        </mu-button>
      </template>
      <mu-carousel-item>
        <img :src="carouselImg1" class="img" />
      </mu-carousel-item>
      <mu-carousel-item>
        <img :src="carouselImg2" class="img" />
      </mu-carousel-item>
      <mu-carousel-item>
        <img :src="carouselImg3" class="img" />
      </mu-carousel-item>
    </mu-carousel>
    <mu-row>
      <mu-col span="12" lg="4" sm="6"> </mu-col>
    </mu-row>

    <p class="title">预警信息</p>
    <mu-row class="hint">
      <mu-sub-header class="sunHeader">预警程度</mu-sub-header>
      <mu-chip class="demo-chip">
        <mu-icon left vlaue=""></mu-icon>普通
      </mu-chip>
      <mu-chip class="demo-chip">
        <mu-icon left vlaue=""></mu-icon>警告
      </mu-chip>
      <mu-chip class="demo-chip">
        <mu-icon left vlaue=""></mu-icon>严重
      </mu-chip>
    </mu-row>

    <mu-tabs
      :value.sync="active2"
      color="green"
      indicator-color="yellow"
      full-width
    >
      <mu-tab>消息预警</mu-tab>
      <mu-tab>传感器预警</mu-tab>
    </mu-tabs>
    <mu-row class="listWarp">
      <mu-col span="12" lg="4" sm="6">
        <mu-list>
          <mu-sub-header>消息预警</mu-sub-header>
          <mu-list-item avatar :ripple="false" button>
            <mu-list-item-action>
              <mu-avatar>
                <img src="../../assets/images/avatar1.jpg" />
              </mu-avatar>
            </mu-list-item-action>
            <mu-list-item-content>
              <mu-list-item-title>这个周末一起吃饭么?</mu-list-item-title>
              <mu-list-item-sub-title>
                <span style="color: rgba(0, 0, 0, 0.87)">Myron Liu -</span>
                周末要来你这里出差，要不要一起吃个饭呀，实在编不下去了,哈哈哈哈哈哈
              </mu-list-item-sub-title>
            </mu-list-item-content>
          </mu-list-item>
        </mu-list>
      </mu-col>
    </mu-row>
  </div>
</template>

<script lang="ts">
</script>

<style lang="scss">
.waring {
  .title {
    margin: 80px 0;
    font-size: 80px;
    &::before {
      content: "";
      padding-left: 30px;
      border-left: 20px #ff6f00 solid;
    }
  }
  .weather {
    .item {
      width: 520px;
      height: 300px;
      margin: 20px auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
      .icon {
        margin: 20px auto;
      }
    }
  }
}
</style>
