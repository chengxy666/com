<template>
  <footer>
    <div class="main">
      <div class="us">
        <div class="left">
          <p>电话：021-55225280</p>
          <p>服务热线：4008 203 808</p>
          <p>网站：www.sevenfiter.com.cn</p>
        </div>
        <div class="right">
          <img src="https://s1.ax1x.com/2020/06/28/NRlgFx.th.jpg" alt />
        </div>
      </div>
      <div class="check">
        <p>©2019 上海途健体育发展有限公司 版权所有</p>
        <p>技术支持：×××</p>
      </div>
    </div>
  </footer>
</template>
<style scoped lang='scss' >
@mixin clearfix {
  &:after {
    clear: both;
    content: ".";
    display: block;
    height: 0;
    line-height: 0;
    overflow: hidden;
  }
  *height: 1%;
}
footer {
  background: #eee;
  .main {
    margin: 0 auto;
    width: 1200px;
    .us {
      padding: 30px;
      width: 400px;
      height: 160px;
      float: right;
      display: flex;
      font-size: 14px;
      color: #666;
    }

    .check {
      clear: both;
      // margin: 10px 0;
      font-size: 12px;
      color: #666;
      text-align: center;
      zoom: 1;
      p {
        padding-bottom: 10px;
      }
    }
  }
}
</style>