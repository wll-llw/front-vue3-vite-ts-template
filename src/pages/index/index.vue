<template>
  <CustomNavbar/>
  <view class="content">
    {{ title }}
  </view>
</template>
<script setup lang="ts">
import { ref } from 'vue'
import CustomNavbar from "./components/CustomNavbar.vue";
const title = ref('Hello')
</script>

<style>
.content {
}

</style>
