<template>
  <mu-appbar style="width: 100%" color="primary" class="topBar">
    <mu-menu slot="left">
      <mu-button icon class="icon">
        <mu-icon value="menu"></mu-icon>
      </mu-button>
      <mu-list slot="content">
        <mu-list-item button>
          <mu-list-item-content>
            <mu-list-item-title>Menu Item 1</mu-list-item-title>
          </mu-list-item-content>
        </mu-list-item>
        <mu-list-item button>
          <mu-list-item-content>
            <mu-list-item-title>Menu Item 2</mu-list-item-title>
          </mu-list-item-content>
        </mu-list-item>
      </mu-list>
    </mu-menu>

    <div>当前时间</div>
  </mu-appbar>
</template>

<script lang="ts">
</script>

<style lang="scss">
.topBar {
  .icon {
    margin-top: 20px;
  }
}
</style>
