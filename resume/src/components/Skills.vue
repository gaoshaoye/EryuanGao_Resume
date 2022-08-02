<template>
  <div class="Eryuan-resume-skills mt-18">
    <div class="Eryuan-resume-h1">Skills</div>
    <BulletPoint v-for="(text,i) in textList" :key="i" :text="text" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BulletPoint from "@/components/BulletPoint.vue";

export default defineComponent({
  name: 'ResumeSkills',
  components: {
    BulletPoint,
  },
  data(){
    return{
      textList: [
        'Programming Languages: JavaScript,C++, Python, Vue.js, jQuery, TypeScript, SCSS, Shell',
        'IDEs: Anaconda, Visual Studio, Xcode, Android Studio',
        'Cloud Platforms: AWS, Google Cloud Platform, Alibaba Cloud Platform',
        'Machine Learning and Artificial Intelligence skills: Natural Language Processing, Deep Learning, Neural Networks, Machine vision,Data Mining',
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
