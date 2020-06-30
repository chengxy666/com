<template>
  <div class="main">
    <!-- 头部广告 -->
    <div class="banner"></div>
    <div class="case">
      <div class="title">
        <p class="chtitle">项目案例</p>
        <p class="entitle">CASE</p>
      </div>
      <div class="case-item">
        <el-tabs v-model="activeName">
          <el-tab-pane label="企业事业单位" name="first">
            <el-row :gutter="20"> 
              <el-col :span="6" v-for="(item,index) in procase.business" :key="index">
                  <div class="show">
                      <div>
                          <img :src="item.img" alt="">
                      </div>
                      <div class="text">{{item.title}}</div>
                  </div>
              </el-col>
            </el-row>
          </el-tab-pane>
          <el-tab-pane label="健身中心俱乐部" name="second">配置管理</el-tab-pane>
          <el-tab-pane label="酒店水疗中心" name="third">角色管理</el-tab-pane>
          <el-tab-pane label="房产社区" name="fourth">定时任务补偿</el-tab-pane>
        </el-tabs>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeName: "first",
      procase: {
        business: [
          {
            id: 1,
            img:
              "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgpIq49gUooOjN0wIwuAg4uAg.jpg",
            title: "东莞厚街尚飞健身"
          },
          {
            id: 1,
            img:
              "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgpIq49gUooOjN0wIwuAg4uAg.jpg",
            title: "东莞厚街尚飞健身"
          },
          {
            id: 1,
            img:
              "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgpIq49gUooOjN0wIwuAg4uAg.jpg",
            title: "东莞厚街尚飞健身"
          },
          {
            id: 1,
            img:
              "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgpIq49gUooOjN0wIwuAg4uAg.jpg",
            title: "东莞厚街尚飞健身"
          }
        ],
        exercise: [
          {
            id: 1,
            img:
              "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg-f6s9gUos5uh8QUwwAw44gU.jpg",
            title: "东莞厚街尚飞健身"
          },
          {
            id: 1,
            img:
              "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg-f6s9gUos5uh8QUwwAw44gU.jpg",
            title: "东莞厚街尚飞健身"
          }
        ]
      }
    };
  }
};
</script>
<style lang="scss" scoped>
.main {
  .banner {
    height: 300px;
    background: url(https://s1.ax1x.com/2020/06/30/N54wO1.jpg);
    background-size: contain;
  }
  .case {
    margin: 0 auto;
    text-align: center;
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
    .case-item {
      margin: 0 auto;
      .show {
        height: 250px;
        padding: 10px;
        img{
            width: 100%;
        }
        // background: #000;
      }
    }
  }
}
</style>