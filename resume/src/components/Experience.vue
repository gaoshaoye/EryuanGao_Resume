<template>
  <div class="Eryuan-resume-experience">
    <div class="Eryuan-resume-h1">Experience</div>
    <ResumeGroup :start="when" :middle="where" :end="what" />
    <BulletPoint v-for="(text,i) in textList" :key="i" :text="text" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ResumeGroup from "@/components/Group.vue";
import BulletPoint from "@/components/BulletPoint.vue";
export default defineComponent({
  name: 'ResumeExperience',
  components: {
    ResumeGroup,
    BulletPoint,

  },
  data(){
    return{
      when:'Feb 2022 - May 2022',
      where:'GETAU PTY LIMITED | Sydney, Australia',
      what:'Full Stack Developer',
      textList: [
        'Reconstructed both the PC and mobile versions of Getau Service Platform website using Vue, TypeScript, and SCSS based on the UI design; realized 100% of the requirements.',
        "Built the Getau Forum with customized WordPress themes and plugins to increase traffic for Getau business partners; achieved around 5,000 views within 2 months.",
        "Evaluated and discussed the feasibility of over 40 draft pages of 3 major updates for Getau Forum and Getau Service Platform with the UI/UX-design teams base on the performance and time complexity using Figma.",
      ]
    }
  },
  
});
</script>


<style scoped lang="scss">
@import "@/assets/style.scss";
.Eryuan-resume-experience {
  margin-top: 22px;
}

</style>
