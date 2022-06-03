<template>
  <div class="Eryuan-resume-bullet_point">
    <div class="Eryuan-resume-bullet_point__dot"></div>
    <div class="Eryuan-resume-p1">{{ text }}</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "BulletPoint",
  components: {},
  props: {
    text: {
      type: String,
      default: "",
    },
  },

});
</script>

<style lang="scss" scoped>
@import "@/assets/style.scss";
.Eryuan-resume-bullet_point {
  margin-top: 8px;
  display: flex;
  &__dot {
    min-width: 3px;
    height: 3px;
    background: $Prime-Black;
    border-radius: 50%;
    margin-top: 6px;
    margin-left: 3px;
    margin-right: 6px;
  }
}
</style>
