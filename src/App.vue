<template>
  <div class="wrapper">
    <!-- 位置 -->
    <div class="position">
      <span class="iconfont position__icon">&#xe619;</span>
      深圳市罗湖区人民南路2028号金光华广场20楼123号
      <span class="iconfont position__notice">&#xe60b;</span>
    </div>
    <!-- 搜索 -->
    <div class="search">
      <span class="iconfont">&#xe62d;</span>
      <span class="search__text">华润万家 大促销 终极优惠</span>
    </div>
    <!-- banner -->
    <div class="banner">
      <img class="banner__img" src="http://www.dell-lee.com/imgs/vue3/banner.jpg" alt="">
    </div>
    <!-- icons -->
    <div class="icons">
      <div class="icons__item">
        <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/超市.png" alt="">
        <p class="icons__item__desc">超市便利</p>
      </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/菜市场.png"  alt="">
          <p class="icons__item__desc">菜市场</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/水果店.png" alt="">
          <p class="icons__item__desc">水果店</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/鲜花.png" alt="">
          <p class="icons__item__desc">鲜花绿植</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/医药健康.png" alt="">
          <p class="icons__item__desc">医药健康</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/家居.png" alt="">
          <p class="icons__item__desc">家居时尚</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/蛋糕.png" alt="">
          <p class="icons__item__desc">烘培蛋糕</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/签到.png" alt="">
          <p class="icons__item__desc">签到</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/大牌免运.png" alt="">
          <p class="icons__item__desc">大牌免运</p>
        </div>
        <div class="icons__item">
          <img class="icons__item__img" src="http://www.dell-lee.com/imgs/vue3/红包.png" alt="">
          <p class="icons__item__desc">红包套餐</p>
        </div>
    </div>

    <div class="gap">
    </div>
  </div>

  <!-- 底部docker -->
  <div class="docker">
    <div class="docker__item docker__item--active">
      <div class="iconfont">&#xe6f3;</div>
      <div class="docker__title">首页</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe7e5;</div>
      <div class="docker__title">购物车</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe61e;</div>
      <div class="docker__title">订单</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe660;</div>
      <div class="docker__title">我的</div>
    </div>
  </div>
</template>

<style lang="scss">
@import './style/variable.scss';
@import './style/mixins.scss';
  // 顶部
  .wrapper {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: .5rem;
    padding: 0 .18rem;
  }
  // 位置
  .position {
    position: relative;
    padding: .16rem .24rem .16rem 0;
    line-height: .22rem;
    font-size: .16rem;
    color: $contentFontColor;
    @include ellipsis;
    .position__icon {
      position: relative;
      top: .01rem;
      font-size: .2rem;
    }
    .position__notice {
      position: absolute;
      right: 0;
      top: .17rem;
      font-size: .2rem;
    }
  }
  // 搜索
  .search {
    margin-bottom: .12rem;
    line-height: 0.32rem;
    background-color: #f5f5f5;
    color: #B7B7B7;
    border-radius: .16rem;
    .iconfont {
      padding: 0 .08rem 0 .16rem;
      display: inline-block;
      font-size: .16rem;
    }
    &__text {
      display: inline-block;
      font-size: .14rem;
    }
  }
  // banner
  .banner {
    height: 0;
    overflow: hidden;
    padding-bottom: 25.4%;
    &__img {
      width: 100%;
    }
  }
  //icons
  .icons {
    display: flex;
    flex-wrap: wrap;
    margin-top: .16rem;
    &__item {
      width: 20%;
      &__img {
        display: block;
        width: .4rem;
        height: .4rem;
        margin: 0 auto;
      }
      &__desc {
        margin: .06rem 0 .16rem 0;
        text-align: center;
        color: $contentFontColor;
      }
    }
  }

  .gap {
    margin: 0 -.18rem;
    height: .1rem;
    background-color: $contentBgColor;
  }
  // 底部docker
  .docker {
    display: flex;
    box-sizing: border-box;
    position: absolute;
    padding: 0 .18rem;
    left: 0;
    bottom: 0;
    width: 100%;
    height: .49rem;
    border-top: .01rem solid $contentBgColor;
    color: $contentFontColor;
    &__item {
      flex: 1;
      text-align: center;
      .iconfont {
        margin: .07rem 0 .02rem 0;
        font-size: .18rem;
      }
      &--active {
        color: #1FA4FC;
      }
    }
    &__title {
      font-size: .2rem;
      transform: scale(.5, .5);
      transform-origin: center top;
    }
  }
</style>
