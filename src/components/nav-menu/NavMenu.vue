<!-- 顶部导航菜单 -->
<template>
  <div class="nav">
    <el-menu
      text-color="#1D1D1D"
      class="el-menu-demo nav-menu"
      mode="horizontal"
      @select="handleSelect"
    >
      <el-menu-item index="1">
        <div class="logoDiv">
          <img class="logo" src="@/assets/logo.png" alt="在协和" />
        </div>
      </el-menu-item>

      <el-menu-item index="1">
        <div class="item">首页</div>
      </el-menu-item>
      <!-- <el-menu-item index="2">
        <div class="item">核心功能</div>
      </el-menu-item> -->
      <el-menu-item index="2">
        <div class="item">课程表</div>
      </el-menu-item>
      <el-menu-item index="3">
        <div class="item">查成绩</div>
      </el-menu-item>
      <el-menu-item index="5">
        <div class="bt">立即体验</div>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {};
  },
  methods: {
    //当前点击的选项
    handleSelect(key, keyPath) {
      this.$emit("selectChange", key); //向外触发选项改变事件, key是选项序号
    }
  }
};
</script>

<style lang='scss' scoped>
$nav-height: 80px;
$nav-bgColor: rgba(
  $color: #ffffff,
  $alpha: 1
);

.nav {
  width: 100%;
}

.el-menu::after,
.el-menu::before {
  display: none;
}

.nav-menu {
  top: 0;
  width: 100%;
  height: $nav-height;
  background: $nav-bgColor;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .el-menu-item {
    padding: 0 !important;
    height: $nav-height;
    line-height: $nav-height;
    border-bottom: 0 !important;
    font-size: 18px;
    font-family: PingFang SC;
    font-weight: 400;
    line-height: 25px;
    opacity: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .el-item-box {
    margin: 1%;
    color: #304156;
  }
}
.el-menu--horizontal {
  border-bottom: 0 !important;
}

.el-menu-item:not(.is-disabled):focus,
.el-menu-item:not(.is-disabled):hover,
.el-submenu__title:hover {
  background-color: rgba($color: #ffffff, $alpha: 0) !important;
  border-bottom: 0px;
}

.el-menu-item:hover {
  color: #409eff !important;
}

.logoDiv {
  padding-right: 200px;
  display: flex;
}

.logo {
  height: 48px;
}

.bt {
  margin: auto;
  width: 141px;
  height: 48px;
  background: linear-gradient(
    88deg,
    rgba(79, 172, 254, 1) 0%,
    rgba(0, 242, 254, 1) 100%
  );
  opacity: 1;
  border-radius: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
}

.bt:hover {
  color: #409eff !important;
}

.item {
  padding: 0 3%;
}
</style>
