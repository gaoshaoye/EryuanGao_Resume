<template>
  <div class="Eryuan-resume-group mt-18">
    <div class="Eryuan-resume-p1">{{ start }}</div>
    <div class="Eryuan-resume-p1 fw-500">{{ middle }}</div>
    <div class="Eryuan-resume-p1">{{ end }}</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ResumeGroup",
  components: {},
  props: {
    start: {
      type: String,
      default: "",
    },
    middle: {
      type: String,
      default: "",
    },
    end: {
      type: String,
      default: "",
    },
  },
});
</script>

<style lang="scss" scoped>
@import "@/assets/style.scss";
</style>
