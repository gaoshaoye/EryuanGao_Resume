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
      when:'Feb 2022 - Current',
      where:'Getau | Sydney, Australia',
      what:'Front End Developer',
      textList: [
        'According to the demands, select the appropriate vue library, and build the front end of the web page with TypeScript and SCSS.',
        "Proficiency in using PHP, SCSS and jQuery languages to develop WordPress websites, providing functions including Ajax and infinite scrolling, and customized themes and plugins to enhance user's experience.",
        "Fully communicate with the designer, and accurately restore the design drawing according to the designer's Figma design drawings.",
        "Developed IoT code with Arduino sensor for an Android app using machine-learning and IoT techniques.",
        "A task progress bar function (dashboard style) is being independently developed, and the purpose is to put it on GitHub as open source for everyone to use.",
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
