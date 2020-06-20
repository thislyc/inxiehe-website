<!-- 主页 -->
<template>
  <div class="home">
    <!-- 导航栏 -->
    <nav-menu class="with" @selectChange="handSelectChange"></nav-menu>

    <page-one class="with" @showCode="handleShowCode" @toMore="handSelectChange"></page-one>
    <page-two class="with"></page-two>
    <page-three></page-three>
    <page-four class="with"></page-four>
 
    <el-dialog :visible.sync="dialogVisible" width="60%" center>
      <img class="code" src="https://image.jieyou.club/jieyou.club/inxiehe/home/code.png" alt="素材" />
    </el-dialog>
  </div>
</template>

<script>
import NavMenu from "@/components/nav-menu/NavMenu.vue"; //导航栏组件
import PageOne from "@/views/page-1/PageOne"; //第一页
import PageTwo from "@/views/page-2/PageTwo"; //第二页
import PageThree from "@/views/page-3/PageThree"; //第三页
import PageFour from "@/views/page-4/PageFour"; //第四页

export default {
  components: {
    NavMenu,
    PageOne,
    PageTwo,
    PageThree,
    PageFour
  },
  data() {
    return {
      pageIndex: "1", //当前页的序号

      // activeNames: ['nav'], //折叠面板显示导航栏nav

      pageOne: 0, //页面距离窗口顶部的距离
      pageTwo: 0,
      pageThree: 0,
      pageFour: 0,
      pageFive: 0,

      dialogVisible: false
    };
  },
  mounted() {
    this.getPageDistance();
  },
  methods: {
    //拿到每个page页面距窗体顶部的距离
    getPageDistance() {
      this.pageOne = document.getElementById("page-one").offsetTop;
      this.pageTwo = document.getElementById("page-two").offsetTop;
      this.pageThree = document.getElementById("page-three").offsetTop;
      this.pageFour = document.getElementById("page-four").offsetTop;
    },

    //选项改变的回调函数, 设置滚动到对应的page
    handSelectChange(index) {
      switch (index) {
        case "1":
          this.pulleyRoll(this.pageOne);
          break;
        case "2":
          this.pulleyRoll(this.pageTwo);
          break;
        case "3":
          this.pulleyRoll(this.pageThree);
          break;
        case "4":
          this.pulleyRoll(this.pageFour);
          break;
        case "5":
          this.handleShowCode();
          break;
      }
    },

    //处理显示二维码的方法
    handleShowCode() {
      this.$data.dialogVisible = true;
    },

    // top是page距窗体顶部的距离
    pulleyRoll(top) {
      //设置页面滚动到的的位置
      window.scrollTo({
        top: top,
        behavior: "smooth"
      });
    }
  }
};
</script>

<style lang='scss' scoped>
.home {
  width: 100%;
}

.code {
  width: 100%;
}

.with{
  width: 86%;
  margin: 0 auto;
}

</style>
