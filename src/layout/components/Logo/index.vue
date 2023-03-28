<script setup lang="ts">
import { websiteConfig } from '@/config/website.config'

defineProps<{ collapsed: boolean }>()
</script>

<template>
  <div class="logo">
    <img :src="websiteConfig.logo" alt="" />
    <h2 v-show="!collapsed" class="title">{{ websiteConfig.title }}</h2>
  </div>
</template>

<style lang="less" scoped>
.logo {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 64px;
  line-height: 64px;
  overflow: hidden;
  white-space: nowrap;

  img {
    width: auto;
    height: 32px;
  }

  .title {
    margin: 0;
    margin-left: 15px;
  }
}
</style>
