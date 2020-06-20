<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },

  created() {
    /**
     * 以768px为断点；判断是手机还是PC；
     * 是手机则设置无法缩放；走手机组件。
     * 是PC则缩放；走PC组件。
     */

    /**
     * 根据页面宽度去replace不一样的界面进来。PC/Phone
     * 1. 一进系统就直接replace不同的页面；之后就是走在两条路上；也就不存在一直要用if else语句；每个父页面Push下去的子页面就是在各自的路上；就不会引发问题。
     * 2. 逻辑是同一个逻辑；但是UI是不同的。在这里；逻辑是固定点；UI是变化的。
     * 3. 每一个Controller都把export default的对象拿出来作为公共对象；放在js文件里。Function不变；写两套、三套template和CSS就成。
     * 4. PC和iPad要一个版本兼容 => 只有Mobile时才固定死viewport => 用js做到。
     * 5. Mobile作等比例布局 vw + rem => 兼容所有手机。
     */
    // let screenWidth = window.screen.width;
    // if (screenWidth < 768) {
    //   let viewport = document.querySelector("meta[name=viewport]");
    //   viewport.setAttribute(
    //     "content",
    //     "user-scalable=no, width=device-width, initial-scale=1.0"
    //   );
    //   this.$router.replace("/mobileHome");
    // } else {
      // this.$router.replace("/");
    // }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width:100%;
  min-width: 1000px;
  max-width: 1920px;
  margin: 0 auto;
}

/* 默认文字颜色 */
.default-text-color{
  color: #304156;
}

  .el-dialog {
    background-color: rgba(0,0,0, 0) !important;
    -webkit-box-shadow: none !important;
    box-shadow: none !important;
  }

  .el-dialog__header{
    display: none;
  }

  .el-dialog__body {
    padding: 0 !important;
  }

</style>
