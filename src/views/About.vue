<template>
  <div class="main">
    <!-- 头部广告 -->
    <div class="banner"></div>
    <div class="us">
      <div class="title">
        <p class="chtitle">联系我们</p>
        <p class="entitle">CONTACT US</p>
      </div>
      <div class="item">
        <el-row>
          <el-col :span="10">
            <div class="tips">我们希望提供真正的解决方案，提供高质量的产品，同时为新的健身模式带来创新。</div>
            <div class="about">
              <p class="com">上海途健体育发展有限公司</p>
              <div about-item>
                <p>地址：上海市闵行区泰虹路168弄万科时一区T1栋808</p>
                <p>网址：www.topgym.cn</p>
                <p>电话：021-55225280</p>
                <p></p>
              </div>
            </div>
          </el-col>
          <el-col :span="10" :offset="4">
            <img src="https://s1.ax1x.com/2020/06/28/N2aAJA.png" alt />
          </el-col>
        </el-row>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.main {
  .banner {
    height: 300px;
    background: url(https://s1.ax1x.com/2020/07/03/NOdulR.jpg);
    background-size: contain;
  }
  .us {
    margin: 0 auto;
    width: 1000px;
    .title {
      padding-top: 65px;
      text-align: center;
      .chtitle {
        color: #333;
        font-size: 24px;
      }
      .entitle {
        color: #999;
        font-size: 12px;
        line-height: 28px;
      }
    }
    .tips {
      font-size: 14px;
      color: #808080;
    }
    .about {
      margin-top: 20px;
      p {
        padding: 10px;
      }
      .com {
        font-size: 20px;
      }
      img {
        width: 100%;
      }
    }
  }
}
</style>
