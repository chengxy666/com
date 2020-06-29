<template>
  <header>
    <el-row>
      <el-col :span="4">
        <div class="grid-conten">
          <img src="https://s1.ax1x.com/2020/06/28/N2aAJA.png" alt />
        </div>
      </el-col>
      <el-col :span="14">
        <div class="grid-content">
          <el-menu
            :default-active="activeIndex"
            class="el-menu-demo"
            mode="horizontal"
            @select="handleSelect"
          >
            <el-menu-item index="1">首页</el-menu-item>
            <el-menu-item index="2">品牌介绍</el-menu-item>
            <el-submenu index="3">
              <template slot="title">产品中心</template>
              <el-menu-item index="3-1">跑步机</el-menu-item>
              <el-menu-item index="3-2">其他有氧</el-menu-item>
              <el-menu-item index="3-3">双功能力量</el-menu-item>
              <el-menu-item index="3-4">单功能力量</el-menu-item>
              <el-menu-item index="3-5">自由力量</el-menu-item>
              <el-menu-item index="3-6">挂片式力量</el-menu-item>
              <el-menu-item index="3-7">个性化系列</el-menu-item>
            </el-submenu>
            <el-submenu index="4">
              <template slot="title">项目案例</template>
              <el-menu-item index="4-1">企业事业单位</el-menu-item>
              <el-menu-item index="4-2">健身中心俱乐部</el-menu-item>
              <el-menu-item index="4-3">酒店水疗中心</el-menu-item>
              <el-menu-item index="4-4">房产社区</el-menu-item>
            </el-submenu>
            <el-submenu index="5">
              <template slot="title">新闻资讯</template>
              <el-menu-item index="5-1">公司新闻</el-menu-item>
              <el-menu-item index="3-2">行业资讯</el-menu-item>
            </el-submenu>
            <el-menu-item index="3">联系我们</el-menu-item>
          </el-menu>
        </div>
      </el-col>
      <el-col :span="4">
        <div class="grid-content bg-purple search">
          <el-input placeholder="请输入内容" v-model="kwd">
            <i slot="prefix" class="el-input__icon el-icon-search"></i>
          </el-input>
        </div>
      </el-col>
    </el-row>
  </header>
</template>
<style lang='scss'>
header {
  width: 1200px;
  margin: 0 auto;
  .el-menu.el-menu--horizontal {
    border-bottom-style: none;
  }
  .search{
    margin-top: 10px;
  }
}
</style>
<script>
export default {
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1",
      kwd:''
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>