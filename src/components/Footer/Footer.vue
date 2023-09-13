<template>
  <div class="footer">
    <div class="footer-left">
      <p class="thank">Thank For</p>
      <p class="site-info">
        <span><img src="../../assets/my/tencent.png" alt="">腾讯云服务器</span>
        <span><img src="../../assets/my/tencent.png" alt="">腾讯云SSL证书</span>
        <span><img src="../../assets/my/tencent.png" alt="">阿里云存储</span>
      </p>
      <p class="version">
        <span>version</span>
        <span>1.1.0</span>
      </p>
      <p>建站日期：2023-09-10</p>
      <p class="beian">
        <img src="../../assets/my/badges.png" alt=""><a href="https://beian.miit.gov.cn">湘ICP备2021010654号-4</a>
      </p>
    </div>
    <div class="footer-right">
      <div class="contact">
        <div>
          <img class="svg" src="../../assets/my/qq_svg.svg" alt="">
          <img class="qq" src="../../assets/my/QQ.jpg" alt="">
        </div>
        <div>
          <img class="svg" src="../../assets/my/wexin_icon.svg" alt="">
          <img class="qq" src="../../assets/my/wx2.jpg" alt="">
        </div>
        <div>
          <a href="https://www.bilibili.com/video/BV1Zy4y1K7SH" target="_blank"><img class="svg" src="../../assets/my/bilibili_icon.svg" alt=""></a>
        </div>
        <div>
          <a href="https://github.com/shenmingLiveYou" target="_blank"><img class="svg" src="../../assets/my/github_icon.svg" alt=""></a>
        </div>
      </div>
      <p>联系邮箱：2807747262@qq.com</p>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "Footer-info",
};
</script>

<script lang="ts" setup></script>

<style scoped lang="less">
.footer {
    width: 100%;
    height: 180px;
    display: flex;
    font-size: 14px;
    border-top: 1px solid #ccc;
    .footer-left,.footer-right {
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .thank {
      color: #26c6e1;
      font-size: 20px;
    }
    .site-info {
      display: flex;
      align-items: center;
      span {
        margin-right: 10px;
        display: flex;
        align-items: center;
      }
      img {
        width: 20px;
        margin-right: 5px;
      }
    }
    .version {
      display: flex;
      span {
        background-color: #333333;
        display: flex;
        justify-content: center;
        align-items: center;
        // display: inline-block;
        // text-align: center;
        // line-height: 30px;
        color: white;
        height: 30px;
        width: 60px;
        font-weight: 600;

        &:nth-child(1) {
          background-color: #ff9800;
          border-radius: 5px 0 0 5px;
        }
        &:nth-child(2) {
          background-color: #26c6da;
          border-radius: 0 5px 5px 0;
        }
      }
    }
    .beian {
      display: flex;
      align-items: center;
    }

    p {
      margin-bottom: 10px;
    }

    .contact {
      width: 250px;
      display: flex;
      justify-content: space-between;
      > div {
        position: relative;
        .qq {
          width: 80px;
          opacity: 0;
          position: absolute;
          top: -30px;
          left: -20px;
          transition: all 0.4s;
        }
      }
    }
    .svg {
          width: 40px;
          cursor: pointer;
          position: relative;
          z-index: 1;
          &:hover {
            & ~ .qq {
                opacity: 1;
                top: -84px;
                left: -20px;
              }
          }
        }
}
</style>