<template>
  <div class="project">
    <global-header></global-header>
    <Content></Content>
    <Footer></Footer>
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import GlobalHeader from '../../components/GlobalHeder/Header.vue';
import Footer from '../../components/Footer/Footer.vue';
import Content from '../../components/Content/Content.vue';
import 'normalize.css';
import '../../style/index.scss';

export default defineComponent({
  components: {
    GlobalHeader,
    Footer,
    Content,
  },
});
</script>

<style lang="scss" scoped>
.project {
  position: relative;
}
</style>
