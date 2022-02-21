<template>
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
    <div class="icons__item" v-for="(item, index) in iconList" :key="index">
      <img class="icons__item__img" :src="`http://www.dell-lee.com/imgs/vue3/${item.imgName}.png`" alt="">
      <p class="icons__item__desc">{{item.desc}}</p>
    </div>

  </div>
  <div class="gap">
  </div>
</template>

<script>
export default {
  name: 'Static',
  setup() {
    const iconList = [
      { imgName: '蛋糕', desc: '烘焙蛋糕'},
      { imgName: '超市', desc: '超市便利'},
      { imgName: '菜市场', desc: '菜市场'},
      { imgName: '水果店', desc: '水果店'},
      { imgName: '鲜花', desc: '鲜花绿植'},
      { imgName: '医药健康', desc: '医药健康'},
      { imgName: '家居', desc: '家居时尚'},
      { imgName: '签到', desc: '签到'},
      { imgName: '大牌免运', desc: '大牌免运'},
      { imgName: '红包', desc: '红包套餐'}
    ]
    return {
      iconList
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '../../style/variable.scss';
  @import '../../style/mixins.scss';
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
</style>
