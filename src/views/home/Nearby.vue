<template>
  <!-- 附近店铺 -->
  <div class="nearby">
    <h3 class="nearby__title">附近店铺</h3>
    <div class="nearby__item" v-for="item in nearbyList" :key="item.id">
      <img class="nearby__item__img" :src="item.imgUrl" alt="">
      <div class="nearby__content">
        <div class="nearby__content__title">{{item.title}}</div>
        <div class="nearby__content__tags">
          <span class="nearby__content__tag" v-for="(innerItem, innerIndex) in item.tags" :key="innerIndex.index">{{innerItem}}+</span>
        </div>
        <p class="nearby__content__highlight">{{item.desc}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Nearby',
  setup() {
    const nearbyList = [
      {
        id: 1,
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送20元', '运费全免'],
        desc: '会员享受满100减40(本月内)'
      },
      {
        id: 2,
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送20元', '运费全免'],
        desc: '会员享受满100减40(本月内)'
      }
    ];
    return {
      nearbyList
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '../../style/variable.scss';
  @import '../../style/mixins.scss';
  // 附近店铺
  .nearby {
    &__title {
      margin: .16rem 0 .04rem 0;
      font-size: .18rem;
      font-weight: 400;
      color: $contentFontColor;
    }
    &__item {
      display: flex;
      &__img {
        margin-right: .16rem;
        width: .56rem;
        height: .56rem;
      }
    }
    &__content {
      flex: 1;
      padding-bottom: .12rem;
      border-bottom: 1px solid $contentBgColor;
      &__title {
        line-height: .22rem;
        font-size: .16rem;
        color: $contentFontColor;
      }
      &__tags {
        margin-top: .08rem;
        line-height: .18rem;
        font-size: .13rem;
      }
      &__tag {
        margin-right: .16rem;
      }
      &__highlight {
        margin: .08rem 0 0 0;
        color: #E93B3B;
        line-height: .18rem;
        font-size: .13rem;
      }
    }
  }
</style>
