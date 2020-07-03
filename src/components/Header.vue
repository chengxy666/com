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
            :default-active="this.$route.path"
            class="el-menu-demo"
            mode="horizontal"
            @select="handleSelect"
            router
            active-text-color="#B9984D"
          >
            <el-menu-item index="/">首页</el-menu-item>
            <el-menu-item index="/brand">品牌介绍</el-menu-item>
            <el-menu-item index="/product">产品中心</el-menu-item>
            <el-menu-item index="/case">项目案例</el-menu-item>
            <el-submenu index="5">
              <template slot="title">新闻资讯</template>
              <el-menu-item index="5-1">公司新闻</el-menu-item>
              <el-menu-item index="3-2">行业资讯</el-menu-item>
            </el-submenu>
            <el-menu-item index="/about">联系我们</el-menu-item>
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
<style lang='scss' scoped>
header {
  width: 1200px;
  margin: 0 auto;
  .el-menu.el-menu--horizontal {
    border-bottom-style: none;
  }
  .search {
    margin-top: 10px;
  }
}
</style>
<script>
export default {
  data() {
    return {
      activeIndex: "/",
      kwd: ""
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>