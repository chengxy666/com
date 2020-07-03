<template>
  <div class="main">
    <!-- 头部图片 -->
    <div class="banner"></div>
    <!-- 品牌介绍 -->
    <div class="product">
      <div class="title">
        <p class="chtitle">品牌介绍</p>
        <p class="entitle">PRODUCTS</p>
      </div>
      <div class="info">
        <el-row>
          <el-col :span="12">
            <div>
              <img
                class="img"
                src="http://20262608.s21i.faiusr.com/4/ABUIABAEGAAgxM_Y6wUoxO6byAQwvAU4rgI.png"
                alt
              />
            </div>
          </el-col>
          <el-col :span="12">
            <div class="detail">
              <p>
                SevenFiter 施菲特作为国际化的
                <span class="exp">商用健身器材品牌</span>,始终坚持“国际品质 智造健康”品牌发展定位，将国际化商用健身器材顶级品牌作为企业未来的发展蓝图，为更好的优化品牌产品与服务，SevenFiter 施菲特技术小组在全球设立2个研发中心，从多维度收集信息，并根据国际前沿的健身体系来研发产品，旨在打造出真正满足市场和用户需求的高品质健身设备。
              </p>
              <p>SevenFiter 施菲特坚持按照国际标准制造生产产品，真正做到从根源处出发，达到优化产品结构和技术创新，打造“国际品质 个性定制 智能互联 ”的品牌形象，为企业健康发展保驾护航。</p>
              <p>SevenFiter 施菲特本着“专业专注 智享全球”的服务理念，严格把控每一个研发阶段，以确保产品每一个部件在进行大规模生产之前，均经过精心的设计、检验与测试，从而带给使用者更加舒适的运动体验。</p>
              <p>SevenFiter 施菲特产品通过ISO9001、ISO14001、OHSAS18001等三大国际管理体系认证，在2018年T7系列跑步机凭借智能化的创新技术荣获“十佳创新产品”荣誉称号，并在2019年健身器材行业十大品牌全国评选活中荣获”精益创新十佳品牌”和”行业百强”企业称号。在未来的发展建设中SevenFiter施菲特将以卓越技术工艺打造高品质产品，以专业团队量身定制服务为基础，深耕中国商用健身器材市场。</p>
            </div>
          </el-col>
        </el-row>
      </div>
    </div>
    <!--  资质荣誉-->
    <div class="honor">
      <div class="title">
        <p class="chtitle">资质荣誉</p>
        <p class="entitle">Qualification Honor</p>
      </div>
      <div class="info">
          <el-row :gutter="20">
              <el-col :span="6" v-for="(item,index) in honor" :key="index" class="info-item">
                  <div>
                      <img :src="item.img" alt="">
                  </div>
                  <div class="text">{{item.title}}</div>
              </el-col>
          </el-row>
          
      </div>
    </div>
  </div>
</template>
<script>
export default {
    data(){
        return{
            honor:[
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            },
                {
                hid:1,
                img:'http://20262608.s21i.faiusr.com/2/ABUIABACGAAg25P17AUoz_-k9wQwhhQ4uQ8.jpg',
                title:'SevenFiter荣获精益创新十佳品牌'
            }
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
.banner {
  height: 300px;
  background: url(https://s1.ax1x.com/2020/06/30/N4XxUA.jpg);
  background-size: contain;
}
.product {
  margin: 0 auto;
  width: 1200px;
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

  .info {
    .img {
      width: 100%;
    }
    .detail {
      padding: 0 10px;
      p {
        text-indent: 2em;
        font-size: 14px;
        span {
          color: #999;
          cursor: pointer;
          text-decoration: underline;
        }
      }
    }
  }
}
.honor {
  margin: 0 auto;
  width: 1200px;
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
  .info{
      .info-item{
          margin: 20px 0;
      img{
          width: 100%;
      }
      .text{
          font-size: 14px;
          padding-top: 10px;
      }
      }
  }
}
</style>