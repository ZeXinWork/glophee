<template>
  <div class="footer">
    <div class="footer__container">
      <div class="footer__container__helper">
        <div><img src="../../assets/foot_logo.svg" alt="footer__logo" /></div>
        <div class="footer__container__helper__text">
          Please feel free to contact us if you have any questions, we’ll do our best to offer help
        </div>
      </div>
      <div class="footer__container__connect">
        <div class="footer__container__connect__header">CONTACT US</div>
        <div class="footer__container__connect__body" v-for="item of contactList" :key="item">
          {{ item }}
        </div>
        <div class="footer__container__connect__img">
          <div @click="handlerTwitter">
            <img src="../../assets/twitter.svg" alt="twitter" class="twitter cursor" />
          </div>
          <div @click="handlerFacebook">
            <img src="../../assets/facebook.svg" alt="facebook" class="cursor" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue';

// 处理点击平台跳转
const useAccountEffect = () => {
  const handlerTwitter = () => {
    console.log('handlerTwitter');
  };
  const handlerFacebook = () => {
    console.log('handlerFacebook');
  };
  return { handlerTwitter, handlerFacebook };
};

// 获取联系账号描述列表
const useConnectEffect = () => {
  const contactList = [
    'Address: 714, building 1, Wuhua Building',
    'E-mail: contact@xmwefun.com',
    'Telephone Number: 8866909',
  ];
  return { contactList };
};

export default defineComponent({
  setup() {
    const { contactList } = useConnectEffect();
    const { handlerTwitter, handlerFacebook } = useAccountEffect();
    return { contactList, handlerTwitter, handlerFacebook };
  },
});
</script>

<style lang="scss" scoped>
@import '@/style/viriables.scss';
@import '@/style/mixins.scss';
.footer {
  width: 100%;
  position: absolute;
  height: 33.1rem;
  left: 0rem;
  bottom: 0rem;
  background: $bg-color;
  padding: 6rem 14.3rem 0 15.3rem;
  box-sizing: border-box;
  &__container {
    display: flex;
    justify-content: space-between;
    &__helper {
      display: flex;
      flex-direction: column;
      &__text {
        width: 23.7rem;
        margin-top: 3rem;
        @include font-Helvetica;
        font-size: 1.4rem;
        line-height: 2rem;
        color: #ffffff99;
      }
    }
    &__connect {
      margin-top: 0.7rem;
      text-align: left;
      width: 28rem;
      &__header {
        @include font-HelveticaStd;
        font-style: normal;
        font-weight: bold;
        font-size: $bold-size;
        line-height: 2.2rem;
        color: #ffffff;
        margin-bottom: 1.3rem;
      }
      &__body {
        @include font-Helvetica;
        font-size: 1.4rem;
        line-height: 2.4rem;
        color: rgba(255, 255, 255, 0.6);
        margin-bottom: 0.6rem;
      }
      &__img {
        display: flex;
        margin-top: 1.3rem;
        .twitter {
          margin-right: 2rem;
        }
        .cursor {
          cursor: pointer;
        }
      }
    }
  }
}
</style>
