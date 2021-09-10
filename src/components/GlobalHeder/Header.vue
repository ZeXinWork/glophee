<template>
  <div class="header">
    <div class="header__logo">
      <img src="../../assets/header_logo.svg" alt="header__logo" />
    </div>
    <div class="header__nav">
      <router-link
        :to="item.name"
        v-for="item in navList"
        :key="item.id"
        :class="{ header__nav__item: true, 'header__nav__item--active': currentIndex === item.id }"
      >
        <span @click="handleSwitch(item.id)">
          {{ item.name }}
        </span>
      </router-link>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from 'vue';

// navList数组属性
export interface navListProps {
  name: string;
  id: number;
  to: {
    name: string;
  };
}

export default defineComponent({
  setup() {
    const navList: Array<navListProps> = [
      {
        name: 'HOME',
        id: 0,
        to: { name: 'Home' },
      },
      {
        name: 'COLLECTION',
        id: 1,
        to: { name: 'Collection' },
      },
      {
        name: 'CONTACT',
        id: 2,
        to: { name: 'Contact' },
      },
    ];
    const currentIndex = ref(0);
    const handleSwitch = (index: number) => {
      currentIndex.value = index;
    };
    return { navList, handleSwitch, currentIndex };
  },
});
</script>

<style lang="scss" scoped>
@import '@/style/viriables.scss';
@import '@/style/mixins.scss';
.header {
  width: 100%;
  &__logo {
    height: 11.2rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  &__nav {
    line-height: 7.4rem;
    box-sizing: border-box;
    background: #ffffff;
    box-shadow: inset 0rem 0.1rem 0rem rgba(216, 216, 216, 0.25);
    margin-left: 3rem;
    text-align: center;
    &__item {
      @include font-HelveticaStd;
      font-weight: 300;
      font-size: $bold-size;
      line-height: 2.2rem;
      text-align: center;
      color: $bg-color;
      cursor: pointer;
      text-decoration: none;
      &--active {
        font-weight: bold;
      }
    }

    &__item:not(:last-child) {
      margin-right: 10rem;
    }
  }
}
</style>
