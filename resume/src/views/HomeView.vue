<template>
  <div class="Eryuan-resume__box">
    <ResumeHeader />
    Eryuan Gao
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ResumeHeader from "@/components/Header.vue";

export default defineComponent({
  name: 'HomeView',
  components: {
    ResumeHeader,
  },
});
</script>
<style lang="scss" scoped>
@import "@/assets/style.scss";
.Eryuan-resume__box {
  background: #ffffff;
  height: 842px;
  width: 595px;
  margin: 40px auto;
}
</style>