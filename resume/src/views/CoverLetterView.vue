<template>

  <div class="Eryuan-resume__box" id="printCV">
    <CLHeader />
    <div>
      <div class="CL__title">
        {{ company }}
        <br/>
        RE: {{ position }}
      </div>
      <div class="CL__content">
        <br/>
        Dear Hiring Manager, 
        <br/>
        I am contacting you to express my interest in the {{ position }} opportunity with {{ company }}. After reviewing the position requirements, I believe that my qualifications and education are a great match. 
        Passionate {{ position }} driven by motivation and desire to learn the field inside and out. Skilled in Vue, Scss, and Typescript, I am able to adapt agile development and drive company results. My experience in Vue development enabled me to switch to React development quickly. With critical thinking and coordination skills, I execute tasks in detail while keeping development progress aligned with project goals and can adapt to changing demands to secure project success. 
        I would greatly appreciate your review of my enclosed resume and outlined credentials. I believe that I can be a valuable addition to {{ company }} and your business goals. At your convenience, I am available for an interview or further discussion. I look forward to your response. 
        <br/>
        <br/>
        Sincerely,
        <br/>
        Eryuan Gao 
      </div>
    </div>

  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import CLHeader from "@/components/CLHeader.vue";


export default defineComponent({
  name: 'CoverLetterView',
  components: {
    CLHeader,
  },
  props: {
    company: {
      type: String,
      default: "公司",
    },
    position: {
      type: String,
      default: "职位",
    },
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
.CL{
  &__title {
    @extend .Eryuan-resume-h2;
    font-size: 18px;
  }
  &__content {
    @extend .Eryuan-resume-p1;
    font-size: 15px;
    line-height: 23px;
  }
}
</style>