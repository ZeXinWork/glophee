<template>
  <div class="title">
    <div class="title__desc">
      <div class="title__desc__header">
        <div><img src="../../assets/title_img.svg" alt="title_img" /></div>
        <div class="title__desc__header__enjoy">ENJOY</div>
        <div>THE</div>
      </div>
      <div>HAPPINESS WITH YOU</div>
    </div>
    <div class="title__button">
      SHOP NOW
      <span class="title__button__right_arrow">
        <img src="../../assets/right_arrow.svg" alt="right_arrow" />
      </span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '@/style/mixins.scss';
.title {
  width: 100%;
  background: url('../../assets/title_bg.png');
  background-size: 100% 100%;
  background-repeat: no-repeat;
  height: 60rem;
  box-sizing: border-box;
  @include flex-coloumnCenter;
  &__desc {
    font-family: Helvetica-Condensed-Black-Se;
    font-style: normal;
    font-weight: 900;
    font-size: 7.2rem;
    text-align: center;
    color: #ffffff;
    /* margin: -10rem 0 0 8rem; */
    &__header {
      display: flex;
      justify-content: center;
      margin-bottom: 2rem;
      &__enjoy {
        margin: 0 6rem 0 4rem;
      }
    }
  }
  &__button {
    width: 25.1rem;
    height: 6.1rem;
    margin-top: 5.2rem;
    background: #fff;
    line-height: 6.1rem;
    border-radius: 3.2rem;
    @include font-Helvetica;
    @include flex-center;
    font-size: 1.3rem;
    color: #333333;
    cursor: pointer;
    transition: all 0.25s;
    &__right_arrow {
      margin: 0.5rem 0 0 1rem;
      display: inline-block;
    }
  }
  &__button:hover {
    animation: hover-bound 0.25s;
    background: #386b7a;
  }

  @keyframes hover-bound {
    0%,
    10%,
    55%,
    90%,
    94%,
    98%,
    100% {
      transform: scale(1, 1);
    }
    30% {
      transform: scale(1.14, 0.86);
    }
    75% {
      transform: scale(0.92, 1.08);
    }
    92% {
      transform: scale(1.04, 0.96);
    }
    96% {
      transform: scale(1.02, 0.98);
    }
    99% {
      transform: scale(1.01, 0.99);
    }
  }
}
</style>
