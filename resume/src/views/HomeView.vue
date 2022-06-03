<template>
  <div class="Eryuan-resume__box">
    <ResumeHeader />
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
  height: 794px;
  width: 507px;
  margin: 40px auto;
  padding: 24px 44px;
}
</style>