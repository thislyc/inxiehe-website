<!-- 第2页 -->
<template>
  <div id="page-two" class="page-two">
    <div class="titleFirst">________&nbsp;&nbsp;一键导课表/分享课表码/即时添加</div>
    <div class="titleSecond">实用的课程表应用，轻松面对数门课程</div>
    <div class="foot">
      <img src="https://image.jieyou.club/jieyou.club/inxiehe/home/page2/left.png" class="left" alt="素材" />
      <div class="right">
        <div class="item" v-for="(item,index) in classList" :key="index">
          <div class="firstRow">
            <img class="icon" :src="'https://image.jieyou.club/jieyou.club/inxiehe/home/page2/'+item.iconName+'.png'" alt="素材" />
            <div class="title">{{item.title}}</div>
          </div>
          <div class="content">{{item.content}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      classList: [
        {
          iconName: "import",
          title: "导入课表",
          content:
            "正方系统的同学可通过自己创建或者他人分享的方式导入课表    18级之后的同学可通过强智系统一键导入课表"
        },
        {
          iconName: "add",
          title: "添加课程",
          content: "课程在被调整时，可即时更改不会落下任何一节课"
        },
        {
          iconName: "qrcode",
          title: "课表码",
          content: "建好课表的同学可将课表码分享给他人    让关系更'进一步'"
        }
      ]
    };
  },
  mounted() {},
  methods: {}
};
</script>

<style lang='scss' scoped>
.page-two {
  width: 100%;
  height: 1220px;
  color: #fff;
  box-sizing: border-box;
  padding-top: 120px;
  .titleFirst {
    font-size: 21px;
    font-family: PingFang SC;
    font-weight: 400;
    line-height: 29px;
    color: rgba(24, 182, 241, 1);
    opacity: 1;
  }
  .titleSecond {
    margin-top: 39px;
    height: 82px;
    font-size: 48px;
    font-family: FZZhengHeiS-R-GB;
    font-weight: 400;
    line-height: 65px;
    color: rgba(51, 51, 51, 1);
    opacity: 1;
  }
  .foot {
    margin-top: 106px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .left {
      width: 55%;
    }
    .right {
      width: 40%;
      .item {
        .firstRow {
          display: flex;
          align-items: center;
          .icon {
            width: 40px;
            height: 40px;
            margin-right: 7px;
          }
          .title {
            height: 59px;
            font-size: 36px;
            font-family: PingFang SC;
            font-weight: 400;
            line-height: 59px;
            color: rgba(51, 51, 51, 1);
            opacity: 0.9;
          }
        }
        .content {
          max-width: 439px;
          padding: 20px 0;
          text-align: left;
          font-size: 16px;
          font-family: PingFang SC;
          font-weight: 400;
          line-height: 26px;
          color: rgba(138, 138, 138, 1);
          opacity: 1;
        }
      }
    }
  }
}

@media screen and (max-width: 1395px) {
  /*当屏幕尺寸小于1395px时，应用下面的CSS样式*/
  .page-two {
    padding-top: 60px;
    .foot {
      margin-top: 30px;
      flex-direction: column;
      .left {
        width: 60%;
      }
    }
  }
}

@media screen and (max-width: 1025px) {
  /*当屏幕尺寸小于1395px时，应用下面的CSS样式*/
  .page-two {
    padding-top: 10px;
    .foot {
      margin-top: 10px;
      flex-direction: column;
      .left {
        width: 80%;
      }
    }
  }
}
</style>