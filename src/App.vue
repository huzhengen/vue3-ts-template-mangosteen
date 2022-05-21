<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
</script>

<template>
  <router-view></router-view>
</template>

<style>
@import './assets/stylesheets/reset.scss';
@import './assets/stylesheets/vars.scss';

html,
body {
  max-width: 480px;
  margin: 0 auto;
}

body {
  font-family: -apple-system, 'Noto Sans', 'Helvetica Neue', Helvetica,
    'Nimbus Sans L', Arial, 'Liberation Sans', 'PingFang SC', 'Hiragino Sans GB',
    'Noto Sans CJK SC', 'Source Han Sans SC', 'Source Han Sans CN',
    'Microsoft YaHei', 'Wenquanyi Micro Hei', 'WenQuanYi Zen Hei', 'ST Heiti',
    SimHei, 'WenQuanYi Zen Hei Sharp', sans-serif;
  font-size: 16px;
  color: #333;
}

::webkit-scrollbar {
  visibility: hidden;
}
</style>
