<template>

          <div class="Eryuan-resume__box">
            <ResumeHeader />
            <ResumeExperience />
            <ResumeSkills />
            <ResumeEducation />
          </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ResumeHeader from "@/components/Header.vue";
import ResumeExperience from "@/components/Experience.vue";
import ResumeSkills from "@/components/Skills.vue";
import ResumeEducation from "@/components/Education.vue";

export default defineComponent({
  name: 'HomeView',
  components: {
    ResumeHeader,
    ResumeExperience,
    ResumeSkills,
    ResumeEducation,

  },
});
</script>
<style lang="scss" scoped>
@import "@/assets/style.scss";
.Eryuan-resume__box {
  background: #ffffff;
  min-height: 794px;
  max-width: 507px;
  margin: 40px auto;
  padding: 24px 44px;
}
</style>