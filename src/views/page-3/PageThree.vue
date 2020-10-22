<!-- 第3页 -->
<template>
  <div>
    <div id="page-three" class="page-three">
      <div class="head">
        <div class="inner">
          <div class="item" v-for="item in count" :key="item.title">
            <div class="title">{{item.number}}</div>
            <div class="line">———</div>
            <div class="des">{{item.des}}</div>
          </div>
        </div>
      </div>
      <!-- ************************ -->
      <div class="center">
        <div class="left">
          <div class="firstRow">
            <div class="line">——</div>
            <div class="eng">&nbsp;Query results</div>
          </div>
          <div class="secondRow">
            查询成绩
            <br />期末/最终/补考/学分
          </div>
          <div class="thirdRow">
            <div class="item">
              <img src="https://image.jieyou.club/jieyou.club/inxiehe/home/page3/1.png" alt="素材" />
              <div class="title">正方系统</div>
              <div class="des">17级及以前</div>
            </div>
            <div class="item">
              <img src="https://image.jieyou.club/jieyou.club/inxiehe/home/page3/2.png" alt="素材" />
              <div class="title">强智系统</div>
              <div class="des">18级及以后</div>
            </div>
          </div>
        </div>
        <img class="right" src="https://image.jieyou.club/jieyou.club/inxiehe/home/page3/right.png" alt="素材" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      count: [
        {
          number: "20K+",
          des: "累计用户"
        },
        {
          number: "700+",
          des: "收藏人数"
        },
        {
          number: "110+",
          des: "封面语"
        },
        {
          number: "2",
          des: "微信/QQ平台"
        }
      ]
    };
  },
  mounted() {},
  methods: {}
};
</script>

<style lang='scss' scoped>
.page-three {
  width: 100%;
  height: 1400px;
  font-size: 50px;
  color: #fff;
  box-sizing: border-box;
}

.head {
  width: 100%;
  height: 280px;
  background: linear-gradient(
    87deg,
    rgba(79, 172, 254, 1) 0%,
    rgba(0, 242, 254, 1) 100%
  );
  opacity: 1;
  .inner {
    margin: auto;
    height: 100%;
    width: 86%;
    display: flex;
    align-items: center;
    justify-content: space-around;
    .item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      .title {
        font-size: 60px;
        font-family: Roboto;
        font-weight: bold;
        line-height: 60px;
        color: rgba(255, 255, 255, 1);
        opacity: 1;
      }
      .line {
        font-size: 50px;
        line-height: 50px;
        color: rgba(255, 255, 255, 1);
        opacity: 1;
      }
      .des {
        font-size: 25px;
        font-family: Roboto;
        font-weight: 400;
        line-height: 25px;
        color: rgba(255, 255, 255, 1);
        opacity: 1;
      }
    }
  }
}

.center {
  margin: 0 auto;
  width: 86%;
  margin-top: 120px;
  display: flex;
  align-items: center;
  .left {
    text-align: left;
    width: 50%;
    .firstRow {
      display: flex;
      align-items: center;
      .line {
        color: rgba(79, 172, 254, 1);
        opacity: 1;
        font-size: 21px;
      }
      .eng {
        font-size: 14px;
        font-family: Roboto;
        font-weight: 400;
        line-height: 50px;
        color: rgba(155, 155, 155, 1);
        letter-spacing: 10px;
        opacity: 1;
      }
    }
    .secondRow {
      height: 146px;
      font-size: 48px;
      font-family: PingFang SC;
      font-weight: 400;
      line-height: 66px;
      color: rgba(23, 16, 99, 1);
      letter-spacing: 3px;
      opacity: 1;
    }
    .thirdRow {
      display: flex;
      .item {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        img {
          width: 62px;
          height: 62px;
          margin-top: 38px;
        }
        .title {
          margin-top: 20px;
          font-size: 20px;
          font-family: PingFang SC;
          font-weight: 400;
          line-height: 46px;
          color: rgba(51, 122, 183, 1);
          letter-spacing: 3px;
          opacity: 1;
        }
        .des {
          font-size: 14px;
          font-family: Poppins;
          font-weight: 400;
          line-height: 28px;
          color: rgba(155, 155, 155, 1);
          letter-spacing: 3px;
          opacity: 1;
        }
      }
      .item:first-child {
        margin-right: 50px;
      }
    }
  }
  .right {
    width: 50%;
  }
}

@media screen and (max-width: 1395px) {
  /*当屏幕尺寸小于1395px时，应用下面的CSS样式*/
  .center {
    flex-direction: column;
    margin-top: 20px;
    .left{
      width: 80%;
    }
    @media screen and (max-width: 1025px) {
      /*当屏幕尺寸小于1395px时，应用下面的CSS样式*/
      .right {
        width: 80%;
      }
    }
  }
}
</style>