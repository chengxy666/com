<template>
  <div class="main">
    <!-- 顶部广告 -->

    <div class="banner"></div>
    <div class="case">
      <div class="title">
        <p class="chtitle">产品中心</p>
        <p class="entitle">PRODUCTS</p>
      </div>

      <div class="item">
        <ul>
          <li v-for="(item,index) in sort" :key="index" @click="getgoods($event)">{{item}}</li>
        </ul>
      </div>

      <div class="goods">
          <el-row :gutter="20">
              <el-col :span="6" v-for="(item,index) in goods" :key="index" class="info-item">
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
  data() {
    return {
      sort: [
        "跑步机",
        "其他有氧",
        "双功能力量",
        "单功能力量",
        "自由力量",
        "挂片式力量",
        "个性化系列"
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
        },
        {
          id: 4,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg3cqH7AUoyK6xswUwoAY4oAY.jpg",
          title: "SF6103模块化绳动训练器"
        },
        {
          id: 4,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg3cqH7AUoyK6xswUwoAY4oAY.jpg",
          title: "SF6103模块化绳动训练器"
        },
        {
          id: 4,
          img:
            "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg3cqH7AUoyK6xswUwoAY4oAY.jpg",
          title: "SF6103模块化绳动训练器"
        }
      ]
    };
  },
  methods: {
    getgoods(e) {}
  },
  mounted(){
    //  this.$axios.get('/goods').then(res=>{
    //      this.goods
    //  })
  }
  
};
</script>
<style lang="scss" scoped>
.main {
  .banner {
    height: 300px;
    background: url(https://s1.ax1x.com/2020/07/03/NOdulR.jpg);
    background-size: contain;
  }
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
  .item {
    width: 1200px;
    margin: 0 auto;
    ul {
      display: flex;
      justify-content: center;
      li {
        margin: 20px;
        cursor: pointer;
      }
    }
  }
  .goods {
          width: 1200px;
          margin:  0 auto;
    .info-item{
        padding-bottom: 30px;
      img{
          outline: 1px solid #ccc;
          width: 100%;
      }
      .text{
          font-size: 14px;
          padding-top: 10px;
          text-align: center;
          cursor: pointer;
      }
      &:hover{
          color: sienna;
      }}
  }
}
</style>