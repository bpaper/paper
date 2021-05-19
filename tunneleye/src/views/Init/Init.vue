
<template>
  <div class="app">
    <div class="head"></div>
    <div class="routerview"></div>
    <div class="buttom"></div>
    <mu-row justify-content="center" class="footerGuide">
      <mu-col span="12">
        <mu-bottom-nav ripple>
          <mu-bottom-nav-item
            value="Location"
            title="人员定位"
            icon="accessibility_new"
          ></mu-bottom-nav-item>
          <mu-bottom-nav-item
            value="PersonInfo"
            title="出勤信息"
            icon="assignment"
          ></mu-bottom-nav-item>
          <mu-bottom-nav-item
            value="Analysis"
            title="环境监测"
            icon="assessment"
          ></mu-bottom-nav-item>
          <mu-bottom-nav-item
            value="Warning"
            title="预警信息"
            icon="info"
          ></mu-bottom-nav-item>
        </mu-bottom-nav>
      </mu-col>
    </mu-row>
  </div>
</template>

<script lang="ts">
</script>

<style lang="scss">
.app {
  .bottom {
    width: 100%;
    height: 300px;
    background-color: #fafafa;
    z-index: 0;
  }
  .footGuide {
    position: fixed;
    width: 100%;
    bottom: 0;
    z-index: 1000;
    background-color: #ffffff;
  }
}
</style>
