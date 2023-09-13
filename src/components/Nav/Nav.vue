<template>
  <div class="nav" ref="nav">
    <div class="left">
        <a href="#">首页</a>
        <a href="#">新闻</a>
        <a href="#">心情</a>
        <a href="#">关于</a>
        <a href="#">文章搜索</a>
        <a href="#">网站导航</a>
        <a href="#">项目相关</a>
        <a href="#">官方文档</a>
    </div>
    <div class="right">
        <el-switch
          @change="changeDark"
          v-model="dark"
          class="mt-2"
          style="margin-right: 20px; padding-bottom: 3px;"
          inline-prompt
          active-icon="MoonNight"
          inactive-icon="Sunny"
        />
        <a href="#">登录</a>
        <a href="#">注册</a>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "Nav-bar",
};
</script>

<script lang="ts" setup>
import { onMounted, ref } from 'vue';

const dark = ref<boolean>(false);
const scroll = ref<number>(240);
const nav:any = ref(null);

const changeDark = () => {
  // 获取HTML根节点
  let html = document.documentElement
  //判断HTML标签是否有类名dark
  dark.value ? (html.className = 'dark') : (html.className = '')
}

const windowScroll = () => {
   // 滚动条距离页面顶部的距离
    let scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
    // 获取所有的a标签
    let a = document.querySelectorAll('a')
    if (scrollTop > scroll.value) {
      nav.value!.style.background = 'white'
      for (const item of a) {
        item.style.color = 'black'
      }
    } else {
      nav.value!.style.background = 'none'
      for (const item of a) {
        item.style.color = 'white'
      }
    }
}

onMounted(()=>{
  window.addEventListener('scroll', windowScroll)
})
</script>

<style scoped lang="less">
.nav {
    width: 100%;
    height: 60px;
    display: flex;
    align-items: center;
    padding: 0 120px;
    // 固定定位
    position: fixed;
    top: 0;
    left: 0;
    z-index: 99;
    .left {
        width: 70%;
    }
    .right {
        width: 30%;
        display: flex;
        justify-content: right;
    }
    a {
        margin-right: 20px;
        &:last-child {
            margin-right: 0;
        }
    }
}
</style>