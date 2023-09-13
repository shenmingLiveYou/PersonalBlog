<template>
  <div class="swiper-container">
    <div class="swiper-img">
      <img src="../../assets//my/img_10.jpg" alt="">
    </div>
    <div class="swiper-img">
      <img src="../../assets/my/wallhaven-ex9gwo_ekTlI2I.png" alt="">
    </div>
    <div class="swiper-img">
      <img src="../../assets/my/wallhaven-l3geq2.jpg" alt="">
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "Swiper-page",
};
</script>

<script lang="ts" setup>
import { nextTick, onUnmounted,} from 'vue';



let timer:any;
nextTick(() => {
  // 获取轮播图div
  let menu_img:any = document.querySelectorAll('.swiper-img');
  // 获取轮播图长度
  let menu_length = menu_img.length;
  // 定义初始位置
  let index = 0;
  // 定义自动轮播
  timer = setInterval(() => {
    index++;
    if (index === menu_length) {
      index = 0;
    }
    for (const item of menu_img) {
      item.style.opacity = 0;
    }
    menu_img[index].style.opacity = 1;
  }, 5000)
})



onUnmounted(() => {
  clearInterval(timer);
})

</script>

<style scoped lang="less">
.swiper-container {
  width: 100%;
  height: 700px;
  position: relative;
  .swiper-img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%; 
    height: 100%;
    overflow: hidden;
    // 设置动画
    transition: all 1s ease-in-out;
    img {
      width: 100%;
    }
  }
}
</style>