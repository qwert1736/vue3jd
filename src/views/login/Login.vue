<template>
  <div class="wrapper">
    <img class="wrapper__img" src="http://www.dell-lee.com/imgs/vue3/user.png" alt="">
    <div class="wrapper__input">
      <input type="text" class="wrapper__input__content" placeholder="请输入手机号">
    </div>
    <div class="wrapper__input">
      <input type="password" class="wrapper__input__content" placeholder="请输入密码">
    </div>
    <div class="wrapper__login-button">登录</div>
    <div class="wrapper__login-register">注册</div>
  </div>
</template>

<script>
export default {
  name: 'Login'
}
</script>

<style lang="scss" scoped>
@import '../../style/variable.scss';

.wrapper {
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  transform: translateY(-50%);
  &__img {
    display: block;
    margin: 0 auto .4rem;
    width: .66rem;
    height: .66rem;
  }
  &__input {
    height: .48rem;
    margin: 0 .4rem .16rem;
    padding: 0 .16rem;
    background-color: #F9F9F9;
    border: 1px solid rgba(0,0,0,.1);
    border-radius: 6px;
    &__content {
      line-height: .48rem;
      border: none;
      outline: none;
      width: 100%;
      background: none;
      font-size: .16rem;
      color: $contentNoticeColor;
      &::placeholder {
        color: $contentNoticeColor;
      }
    }
  }
  &__login-button {
    margin: .32rem .4rem .16rem .4rem;
    line-height: .48rem;
    background-color: #0091FF;
    box-shadow: 0 .04rem .08rem 0 rgba(0,145,255,.32);
    border-radius: .04rem;
    color: #fff;
    font-size: .16rem;
    text-align: center;
  }
  &__login-register {
    text-align: center;
    font-size: .14rem;
    color: $contentNoticeColor;
  }
}
</style>
