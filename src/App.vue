<template>
  <global-header></global-header>
  <router-view />
  <!-- <Footer></Footer> -->
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import GlobalHeader from './components/GlobalHeder/Header.vue';
import Footer from './components/Footer/Footer.vue';
import 'normalize.css';
import './style/index.scss';

export default defineComponent({
  components: {
    GlobalHeader,
    // Footer,
  },
});
</script>

<style lang="scss"></style>
