<!-- 第一页 -->
<template>
  <div>
    <!-- <div id="page-one" class="page-one" :style=" 'height:'+curHeight+'px' ">1</div> -->
    <div id="page-one" class="page-one">
      <div class="rowFirst">
        <div class="left">
          <div class="titleFirst">________&nbsp;&nbsp;上万协和人都在用的校园小程序</div>
          <div class="titleSecond">在协和</div>
          <div class="content">
            在协和小程序是一个目标用户为山东协和学院学生的校园应用。完美融合了学校的教务管理系统，方便协和学子查询成绩，选课等。目前新加入了豆瓣电影，准考证，PPT模板等有趣实用
            的功能，关于校园卡及校园网的相关信息也可供参考。
          </div>
          <div class="bts">
            <div class="bt center leftBt" @click="showCode">Enjoy Now</div>
            <div class="bt center rightBt" @click="toMore">Learn More</div>
          </div>
        </div>
        <div class="right">
          <img class="card1" src="https://image.jieyou.club/jieyou.club/inxiehe/home/page1/right-card1.png" alt="素材" />
          <div class="rightCenter">
            <img class="card2" src="https://image.jieyou.club/jieyou.club/inxiehe/home/page1/right-card2.png" alt="素材" />
            <img class="iphone" src="https://image.jieyou.club/jieyou.club/inxiehe/home/page1/phone.png" alt="素材" />
            <el-carousel
              class="swiper"
              :interval=4000
              height="558px"
              indicator-position="none"
              arrow="nerver"
            >
              <el-carousel-item v-for="item in 3" :key="item">
                <img :src="'https://image.jieyou.club/jieyou.club/inxiehe/home/page1/review/'+item+'.png'" alt="素材" />
              </el-carousel-item>
            </el-carousel>
          </div>
          <img class="card3" src="https://image.jieyou.club/jieyou.club/inxiehe/home/page1/right-card3.png" alt="素材" />
        </div>
      </div>
      <div class="rowSecond">
        <div class="rowItem" v-for="item in subject" :key="item.imgId">
          <img :src="'https://image.jieyou.club/jieyou.club/inxiehe/home/page1/subject/'+item.imgId+'.png'" alt="素材" />
          <div class="title">{{item.title}}</div>
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
      subject: [
        {
          title: "课程表",
          imgId: "1"
        },
        {
          title: "封面语",
          imgId: "2"
        },
        {
          title: "选修课",
          imgId: "3"
        },
        {
          title: "准考证",
          imgId: "4"
        },
        {
          title: "看豆瓣",
          imgId: "5"
        }
      ],
      //curHeight: "" //窗口高度
    };
  },
  methods: {
    //当前点击的选项
    toMore() {
      this.$emit("toMore", "2"); //向外触发选项改变事件, key是选项序号
    },
    showCode(){
      this.$emit("showCode");
    }
  },
  mounted() {
    //var h = document.documentElement.clientHeight || document.body.clientHeight;
    //this.curHeight = h; //获取窗口height
  }
};
</script>

<style lang="scss" scoped>
.page-one {
  width: 100%;
  height: 1000px;

  .rowFirst {
    width: 100%;
    height: 720px;
    display: flex;
    .left {
      width: 50%;
      height: 100%;
      font-size: 50px;
      color: #fff;
      background-color: #ffffff;
      box-sizing: border-box;
      display: flex;
      flex-direction: column;
      text-align: left;
      .titleFirst {
        font-size: 21px;
        font-family: PingFang SC;
        font-weight: 400;
        line-height: 29px;
        color: rgba(24, 182, 241, 1);
        opacity: 1;
        margin-top: 241px;
      }
      .titleSecond {
        margin-top: 40px;
        font-size: 55px;
        font-family: FZZhengHeiS-R-GB;
        font-weight: 400;
        line-height: 65px;
        color: rgba(51, 51, 51, 1);
        opacity: 1;
      }
      .content {
        margin-top: 40px;
        font-size: 15px;
        font-family: PingFang SC;
        font-weight: 400;
        line-height: 27px;
        color: rgba(155, 155, 155, 1);
        opacity: 1;
      }
      .bts {
        font-size: 14px;
        font-family: PingFang SC;
        font-weight: 400;
        line-height: 20px;
        color: rgba(255, 255, 255, 1);
        opacity: 1;
        margin-top: 64px;
        display: flex;
        .leftBt {
          width: 141px;
          height: 48px;
          background: linear-gradient(
            88deg,
            rgba(79, 172, 254, 1) 0%,
            rgba(0, 242, 254, 1) 100%
          );
          opacity: 1;
          border-radius: 24px;
          margin-right: 64px;
        }
        .rightBt {
          width: 141px;
          height: 48px;
          border: 1px solid rgba(51, 122, 183, 1);
          opacity: 1;
          border-radius: 24px;
          color: rgba(51, 122, 183, 1);
        }
      }
    }
    .right {
      -moz-user-select: none;
      -webkit-user-select: none;
      -ms-user-select: none;
      -khtml-user-select: none;
      user-select: none;

      width: 50%;
      height: 100%;
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      .card1 {
        width: 65px;
        height: 178px;
      }
      .rightCenter {
        display: flex;
        align-items: flex-end;
        .card2 {
          width: 168px;
          height: 449px;
          z-index: 1000;
        }
        .swiper {
          margin: auto auto 16px -289px;
          width: 269px;
          z-index: -12;
        }
        .iphone {
          width: 308px;
          height: 590px;
          margin-left: -44px;
          z-index: 999;
        }
      }
      @media screen and (max-width: 1395px) {
        /*当屏幕尺寸小于1395px时，应用下面的CSS样式*/
        .card1 {
          display: none;
        }
        .rightCenter {
          margin: 0 auto;
        }
        .card3 {
          display: none;
        }
      }
      .card3 {
        width: 192px;
        height: 315px;
      }
    }
  }

  .rowSecond {
    margin-top: 100px;
    height: 120px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .rowItem {
      width: 140px;
      height: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      img {
        height: 50px;
        width: 50px;
        margin-bottom: 9px;
      }
      .title {
        height: 21px;
        font-size: 15px;
        font-family: PingFang SC;
        font-weight: 400;
        line-height: 21px;
        color: rgba(51, 51, 51, 1);
        opacity: 1;
      }
    }
  }
}

.el-carousel__item img {
  width: 100%;
  height: 100%;
}

.center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.bt:hover {
  cursor: pointer;
  color: #409eff !important;
}
</style>