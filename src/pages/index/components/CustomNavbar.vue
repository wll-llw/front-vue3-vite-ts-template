<template>
  <view class="navbar" :style="{ paddingTop: safeAreaInsets?.top+'px'}">
    <view class="logo">
      <view class="logo-title">小兔仙儿</view>
      <text class="logo-text">新鲜 · 亲民 · 快捷</text>
    </view>
    <view class="search">
      <input placeholder="搜索商品" v-model="goods">
    </view>
  </view>
</template>

<script setup lang="ts">
import {ref} from "vue";

const goods = ref('')
// 获取屏幕边界到安全区域距离
const { safeAreaInsets } = uni.getSystemInfoSync()
console.log(safeAreaInsets)
</script>

<style lang="scss">
.navbar {
  background-color: #429f95;
  color: #fff;
  padding-bottom: 10px;
  .logo {
    display: flex;
    align-items: center;
  }
  .logo-title {
    font-size: 24px;
    padding: 20px;
  }
  .logo-text {
    border-left: 1px solid #fff;
    padding: 0 20px;
  }
  .search {
    margin: 0 20px;
    height: 30px;
    border: 1px solid #ccc;
    border-radius: 15px;
  }
  input {
    height: 100%;
    padding: 0 15px;
  }
}
</style>
