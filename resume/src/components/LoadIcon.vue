<template>
  <img
    :height="height"
    :width="width"
    :src="require(`@/assets/${iconName}.svg`)"
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "LoadIcon",
  components: {},
  props: {
    iconName: {
      type: String,
      default: "email_icon",
    },
    height: {
      type: String,
      default: "16",
    },
    width: {
      type: String,
      default: "16",
    },
  },
});
</script>

<style lang="scss" scoped></style>
