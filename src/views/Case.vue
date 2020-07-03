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
          <el-tab-pane
            :key="index"
            v-for="(item, index) in className"
            :label="item.title"
            :name="item.name"
          >
            <el-row :gutter="20" class="item">
              <el-col :span="6" v-for="(i,index) in item.business" :key="index">
                <div class="show">
                  <div @click="show()">
                    <img :src="i.img" alt />
                  </div>
                  <div class="text">{{i.title}}</div>
                </div>
              </el-col>
            </el-row>
          </el-tab-pane>
        </el-tabs>
      </div>
    </div>
    <div class="mo" v-show="active">
      <div class="close" @click="show()">
        <i class="el-icon-close"></i>
      </div>
      <el-carousel :interval="2000" type="card" height="80vh" arrow="never">
        <el-carousel-item v-for="(item,index) in className[0].business[0]" :key="index">
          <img :src="item.img" alt />
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeName: 0,
      active: false,
      className: [
        {
          id: 1,
          title: "企业事业单位",
          business: [
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg5_XR9gUotdmbiAMwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgs53B9wUoiInYIDCgCzi4CA.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgsJ3B9wUokpuipAMwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg_ObR9gUopqrzogEwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            }
          ]
        },
        {
          id: 2,
          title: "健身中心俱乐部",
          business: [
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg5_XR9gUotdmbiAMwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身1"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgs53B9wUoiInYIDCgCzi4CA.jpg",
              title: "东莞厚街尚飞健身1"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgsJ3B9wUokpuipAMwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身2"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg_ObR9gUopqrzogEwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身3"
            }
          ]
        },
        {
          id: 3,
          title: "酒店水疗中心",
          business: [
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg5_XR9gUotdmbiAMwoAs4uAg.jpg",
              title: "东厚街尚飞健身2"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgs53B9wUoiInYIDCgCzi4CA.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgsJ3B9wUokpuipAMwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg_ObR9gUopqrzogEwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            }
          ]
        },
        {
          id: 4,
          title: "房产社区",
          business: [
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg5_XR9gUotdmbiAMwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgs53B9wUoiInYIDCgCzi4CA.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAgsJ3B9wUokpuipAMwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            },
            {
              id: 1,
              img:
                "http://20262608.s21i.faiusr.com/2/ABUIABACGAAg_ObR9gUopqrzogEwoAs4uAg.jpg",
              title: "东莞厚街尚飞健身"
            }
          ]
        }
      ],
      procase: {
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
  },
  methods: {
    show() {
      this.active = !this.active;
    }
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
      .item {
        .show {
          height: 250px;
          padding: 10px;
          img {
            width: 100%;
          }
          // background: #000;
        }
      }
    }
  }
  .mo {
    top: 10vh;
    background: rgba(0, 0, 0, 0.5);
    position: absolute;
    width: 100%;
    text-align: center;
    z-index: 100;
    height: 100vh;
    .close {
      margin: 20px;
      width: 50px;
      height: 50px;
      background: #ccc;
      opacity: 0.3;
      border-radius: 50%;
      float: right;
      text-align: center;
      line-height: 50px;
      cursor: pointer;
      &:hover {
        opacity: 1;
      }
    }
    img {
      height: 100%;
    }
  }
}
</style>