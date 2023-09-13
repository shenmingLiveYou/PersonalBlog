<template>
  <div class="main">
    <div class="container">
      <div class="left">
        <div class="card">
          <div class="title">
            <h2>精选文章</h2>
            <div>
              <a href="#">查看更多</a>
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>精选文章</h2>
            <div>
              <a href="#">查看更多</a>
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>精选文章</h2>
            <div>
              <a href="#">查看更多</a>
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>精选文章</h2>
            <div>
              <a href="#">查看更多</a>
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>精选文章</h2>
            <div>
              <a href="#">查看更多</a>
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>精选文章</h2>
            <div>
              <a href="#">查看更多</a>
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
      </div>
      <div class="right">
        <div class="card">
          <div class="title">
            <h2>标签云</h2>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>TODO</h2>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>站点信息</h2>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>意见反馈</h2>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>友情链接</h2>
            <div>
              <a href="#">申请友链</a>
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
        <div class="card">
          <div class="title">
            <h2>个人名片</h2>
            <div>
              <img src="" alt="">
            </div>
          </div>
          <div class="body">
            主要内容区域
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "Main-Info",
};
</script>

<script lang="ts" setup></script>

<style scoped lang="less">
.main {
    padding: 20px 120px;
    display: flex;
    justify-content: center;
    .container{
      width: 1200px;
      min-height: 200px;
      display: flex;
      justify-content: space-between;
      .left {
        width: 69%;
        .card {
          margin-bottom: 20px;
        }
      }
      .right {
        width: 30%;
        .card {
          margin-bottom: 20px;
        }
      }
    }
    a {
      color: #FF9800 !important;
    }
}
.card {
      background-color: #F0EEEE;
      border-radius: 5px;
      .title {
          display: flex;
          justify-content: space-between;
          align-items: center;
          padding: 20px 20px 10px 20px;
          border-bottom: 1px solid #ccc;
      }
      .body {
        padding: 10px 20px 20px 20px;
        border-radius: 0 0 5px 5px;
      }
    }
</style>