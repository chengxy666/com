<template>
  <div class="main">
    <!-- 轮播图 -->
    <el-carousel :interval="5000" arrow="always" height="680px">
      <el-carousel-item v-for="(item,index) in data.banners" :key="index">
        <img :src="item" alt />
      </el-carousel-item>
    </el-carousel>
    <!-- 品牌介绍 -->
    <div class="brand">
      <div class="title">
        <p class="chtitle">品牌介绍</p>
        <p class="entitle">BRAND INTRODUCTION</p>
      </div>
      <div class="detail">
        <el-row :gutter="20">
          <el-col :span="6" v-for="(item,index) in data.brand" :key="index">
            <div class="grid-content bg-purple content">
              <div class="img">
                <img :src="item.icon" alt />
              </div>
              <div class="tips">{{item.title}}</div>
              <div class="details">{{item.detail}}</div>
            </div>
          </el-col>
        </el-row>
      </div>
    </div>
    <!-- 公司介绍 -->
    <div class="profile">
      <div class="info">
        <p>SevenFiter施菲特是国际化商用健身器材品牌，秉承“国际品质，智造健康”的理念。致力于为客户提供课程化、个性化及智能化的健身器材，来成就健身者的训练目标，提高合作伙伴的效益。</p>
        <p>SevenFiter 施菲特技术小组在全球设立2个研发中心，从多维度收集信息，并根据国际前沿的健身体系来研发产品，旨在打造出真正满足市场和用户需求的高品质健身设备。</p>
        <el-button plain class="btn">MORE +</el-button>
      </div>
    </div>
    <!-- 产品展示 -->
    <div class="product">
      <div class="title">
        <p class="chtitle">产品展示</p>
        <p class="entitle">PRODUCTS</p>
      </div>
      <div class="goods">
        <el-row :gutter="20">
          <el-col :span="6" v-for="(item,index) in data.goods" :key="index">
            <div class="grid-content bg-purple">
              <div class="img">
                <img :src="item.img" alt />
              </div>
              <div class="tip">{{item.title}}</div>
            </div>
          </el-col>
        </el-row>
        <div>
          <el-button plain class="btn">MORE +</el-button>
        </div>
      </div>
    </div>
    <!-- 广告 -->
    <div class="ad">
      <div class="title">
        <p class="mainTitle">精品健身工作室 设备配备解决方案</p>
        <p class="Subtitle">帮您打造一个满足该工作室需求的健身空间</p>
      </div>
    </div>
    <!-- 新闻 -->
    <div class="news">
      <div class="title">
        <p class="chtitle">新闻资讯</p>
        <p class="entitle">NEWS</p>
      </div>
      <div class="news-item">
          <div class="item" v-for="(item,index) of data.news" :key="index">
        <el-card shadow="hover" >
            <el-row>
              <el-col :span="6">
                <div>
                  <img class="img" :src="item.img" alt />
                </div>
              </el-col>
              <el-col :span="16">
                <div class="detail">
                  <p class="Title">{{item.title}}</p>
                  <p class="subtitle">{{item.subtitle}}</p>
                  <el-tag type="info" class="tips">{{item.tips}}</el-tag>
                </div>
              </el-col>
              <el-col :span="2">{{item.date}}</el-col>
            </el-row>
        </el-card>
          </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data:{
      banners: [
        "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg8JCC7wUo1uep4wYwgA84oAY.jpg",
        "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg8JCC7wUozqGTyAEwgA843AY.jpg",
        "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgg6Gp8gUo2_el4QEwgA84oAY.jpg",
        "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgxJKh7AUoqtGP8gUwgA843AY.jpg"
      ],
      brand: [
        {
          icon:
            "http://20262608.s21i.faiusr.com/4/ABUIABAEGAAg5LiX6wUo3IWiLTBuOG4.png",
          title: "匠心智造",
          detail: "致力于为客户提供课程化、个性化及智能化的健身器材"
        },
        {
          icon:
            "http://20262608.s21i.faiusr.com/4/ABUIABAEGAAgkLmX6wUonciF8wQwbjhu.png",
          title: "技术支持",
          detail: "在全球设立2个研发制造中心，根据国际前沿的健身体系来研发产品"
        },
        {
          icon:
            "http://20262608.s21i.faiusr.com/4/ABUIABAEGAAgrbmX6wUonfPA8gQwbjhu.png",
          title: "国际标准",
          detail: "以优化产品结构为基础、技术创新为动力，持续健康发展"
        },
        {
          icon:
            "http://20262608.s21i.faiusr.com/4/ABUIABAEGAAgu7mX6wUo_pzxkQUwbjhu.png ",
          title: "体系认证",
          detail: "IOS9001质量管理体系、ISO14001环境管理体系"
        }
      ],
      goods: [
        {
          id: 1,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgmJ7g7QUossSVUjCgBjigBg.jpg",
          title: "T7X商用跑步机"
        },
        {
          id: 2,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgjJbd6wUomsiTqwYwoAY4oAY.jpg",
          title: "SF7201推胸、推肩训练器 "
        },
        {
          id: 3,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAglb2L7AUorJWj2wcwoAY4oAY.jpg",
          title: "E5椭圆机"
        },
        {
          id: 4,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg3cqH7AUoyK6xswUwoAY4oAY.jpg",
          title: "SF6103模块化绳动训练器"
        }
      ],
      news: [
        {
          nid: 1,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgn-y_7QUouJOWzgcwuAg4qgY!700x700.jpg",
          title:
            "大集结，齐分享，共学习，再亮剑！途健第三期健客训练营圆满成功！",
          subtitle:
            "为期两天的健客训练营培训就这样圆满成功。相信大家一定收获满满。“宝剑出鞘，锋芒毕露，健客结义，仗走天涯”。让我们一起亮剑吧！",
          date: "2019-10-23",
          tips: "公司新闻"
        },
        {
          nid: 1,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgn-y_7QUouJOWzgcwuAg4qgY!700x700.jpg",
          title:
            "大集结，齐分享，共学习，再亮剑！途健第三期健客训练营圆满成功！",
          subtitle:
            "为期两天的健客训练营培训就这样圆满成功。相信大家一定收获满满。“宝剑出鞘，锋芒毕露，健客结义，仗走天涯”。让我们一起亮剑吧！",
          date: "2019-10-23",
          tips: "公司新闻"
        }
      ]
    }
    }
  },
  mounted() {
    console.log(this.goods);
  }
};
</script>
<style lang="scss" scoped>
.brand {
  margin: 0 auto;
  width: 1200px;
  height: 500px;
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
  .detail {
    margin: 65px 0;
    text-align: center;
    .content {
      height: 210px;
      .img img {
        width: 90px;
        height: 90px;
      }
      .details {
        margin-top: 10px;
      }
    }
  }
}
.profile {
  height: 500px;
  background: url(https://s1.ax1x.com/2020/06/27/N6fg2D.jpg) 50%;
  .info {
    width: 30%;
    padding-left: 120px;
    padding-top: 60px;
    height: 360px;
    p {
      font-size: 14px;
      color: #353535;
      line-height: 36px;
      letter-spacing: 0.2em;
    }
    .btn {
      margin-top: 60px;
      color: #b9984d;
      background: transparent;
      border: 1px solid #b9984d;
    }
  }
}
.product {
  height: 560px;
  width: 1200px;
  margin: 0 auto;
  text-align: center;
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
  .goods {
    height: 380px;
    .img {
      height: 275px;
      width: 275px;
      img {
        width: 100%;
        height: 100%;
        overflow: hidden;
      }
      &:hover {
        transform: scale(1.2);
      }
    }
    .tip {
      padding-top: 20px;
    }
  }
  .btn {
    margin-top: 40px;
    color: #4c4c4c;
    background: transparent;
    border: 1px solid #4c4c4c;
  }
}
.ad {
  height: 200px;
  background: url(https://s1.ax1x.com/2020/06/29/NfdHSJ.jpg);
  background-size: contain;
  .title {
    height: 45px;
    width: 1200px;
    margin: 0 auto;
    padding: 60px 0;
    text-align: center;
    color: #ffffff;
    .mainTitle {
      font-size: 30px;
    }
    .Subtitle {
      font-size: 20px;
    }
  }
}
.news {
  // height: 1000px;
  width: 1200px;
  margin: 0 auto;
  cursor: pointer;
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
  .news-item {
   padding-top: 20px;
    .item{
      margin-bottom : 10px;
      height: 200px;
      .img {
      width: 220px;
      height: 130px;
    }
    .detail {
      font-size: 12px;
      .Title {
        font-size: 16px;
        padding: 15px 0;
        &:hover{
          color:#b9984d
        }
      }
      .subtitle{
        padding: 15px 0;
      }
    }
    }
  }
}
</style>
