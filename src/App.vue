<script setup lang="ts">
import mainInfo from './views/MainInfo/index.vue'
import Nav from '@/components/Nav/Nav.vue'
import Footer from '@/components/Footer/Footer.vue'
import Swiper from '@/components/Swiper/index.vue'

</script>

<template>
  <!-- 顶部导航栏 -->
  <Nav />
  <!-- 轮播图 -->
  <Swiper />
  <!-- 主体部分 -->
  <mainInfo />
  <!-- 底部展示 -->
  <Footer />
</template>

<style lang="less">
#app {
  width: 100%;
}
</style>
