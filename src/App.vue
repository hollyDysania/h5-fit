<template>
  <div id="app">
    <div class="top">
      <div class="header">我的</div>
      <div class="content">
        <div class="card">
          <img src="./assets/img/avatar.svg" alt="头像" />
          <div class="info">
            <div class="name">嘻嘻嘻</div>
            <div class="member bg-white">
              <i class="iconfont icon-Star"></i>
              二星会员
            </div>
          </div>
          <div class="right"> 
            <i class="iconfont icon-shezhi"></i>
            设置
          </div>
        </div>
      </div>
    </div>
    <div class="add-car bg-card">
      <i class="iconfont icon-add"></i>
      <div class="info">
        <div>添加车型</div>
        <div class="msg">为您推荐合适的商品</div>
      </div>
    </div>
    <div class="order bg-card">
      <div class="header">
        <span class="my">我的订单</span>
        <div>
          <span class="all">全部订单</span>
          <i class="iconfont icon-jiantou"></i>
        </div>
      </div>
      <div class="content">
        <div class="item">
          <i class="iconfont icon-daifukuan"></i>
          待付款
        </div>
        <div class="item">
          <i class="iconfont icon-daifahuo"></i>
          待发货
        </div>
        <div class="item">
          <i class="iconfont icon-daishouhuo"></i>
          待收货
        </div>
        <div class="item">
          <i class="iconfont icon-yiwancheng"></i>
          已完成
        </div>
        <div class="item">
          <i class="iconfont icon-tuikuan"></i>
          退款/收货
        </div>
      </div>
    </div>
    <div class="coupon bg-card">
      <div class="header">
        <span class="my">优惠券</span>
        <div>
          <span class="all">全部订单</span>
          <i class="iconfont icon-jiantou"></i>
        </div>
      </div>
      <div class="header">
        <span class="my">收货地址</span>
        <i class="iconfont icon-jiantou"></i>
      </div>
    </div>
    <ul class="bottom">
      <li v-for="(item, index) in bottomList" :key="index">
        <img :src="require(`@/assets/img/${index}.svg`)" alt="" />
        <span>{{ item }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      bottomList: ["首页", "活动", "购物车", "我的"]
    };
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #f9f9f9;
  min-height: 100vh;
  padding: 0 24px;
  color: #333;
  padding-bottom: 180px;
  .bg-card{
    margin-top: 22px;
    background-color: #fff;
    border-radius: 16px;
  }
  .top {
    .header {
      text-align: center;
      font-size: 35px;
      padding: 24px;
      height: 100px;
      vertical-align: middle;
    }
    .content {
      .card {
        height: 258px;
        border-radius: 16px;
        background-color: #ff8e2c;
        display: flex;
        padding: 24px;
        position: relative;
        align-items: center;
        img {
          width: 128px;
          height: 128px;
          border-radius: 50%;
        }
        .info {
          margin-left: 24px;
          .name {
            font-size: 40px;
            margin-bottom: 16px;
            color: #fff;
          }
          .member {
            background-color: #fff;
            border-radius: 20px;
            font-size: 20px;
            padding: 10px;
            color: #ff8e2c;
            display: inline-block;
            vertical-align: middle;
          }
        }
        .right {
          position: absolute;
          top: 24px;
          right: 24px;
          font-size: 20px;
          display: flex;
          align-items: center;
          justify-content: center;
          color: #fff;
          i {
            font-size: 30px;
            margin-right: 10px;
          }
        }
      }
    }
  }
  .add-car {
    display: flex;
    font-size: 30px;
    height: 140px;
    align-items: center;
    padding: 24px;
    i {
      font-size: 76px;
      margin-right: 24px;
      color: #ff7700;
    }
    .msg {
      color: gray;
      font-size: 26px;
      margin-top: 22px;
    }
  }
  .order {
    .header {
      padding: 24px;
      display: flex;
      height: 90px;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid #f6f6f6;
      .my {
        font-size: 30px;
      }
      .all {
        color: gray;
        font-size: 26px;
      }
    }
    .content {
      display: flex;
      justify-content: space-around;
      .item {
        display: flex;
        flex-direction: column;
        align-items: center;
        font-size: 22px;
        padding: 24px 0;
        color: gray;
        .iconfont {
          font-size: 50px;
          margin-bottom: 18px;
          color: gray;
        }
      }
    }
  }
  .coupon {
    .header {
      padding: 24px;
      display: flex;
      height: 90px;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid #f6f6f6;
      .my {
        font-size: 30px;
      }
      .all {
        color: gray;
        font-size: 26px;
      }
    }
  }
  .bottom {
    position: fixed;
    bottom: 0;
    left: 0;
    display: flex;
    background-color: #fff;
    justify-content: space-around;
    width: 100%;
    margin: 8px 0;
    height: 90px;
    li {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    img {
      height: 54px;
      width: 54px;
      margin-bottom: 8px;
    }
    span {
      font-size: 20px;
    }
  }
}
</style>
