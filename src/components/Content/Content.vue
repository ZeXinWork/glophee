<template>
  <div class="content"><Title></Title></div>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import Title from '../Title/Title.vue';

export default defineComponent({
  components: { Title },
});
</script>

<style lang="scss" scoped>
.content {
  height: 350rem;
}
</style>
