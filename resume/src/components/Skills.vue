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
        'Proficient in using a variety of Programming Languages( JavaScript, Python, Vue.js, jQuery, TypeScript, SCSS, C++)',
        'Proficient in operating several IDEs( Anaconda, Visual Studio, Xcode, Android Studio)',
        'Be able to operate popular Cloud Platforms( AWS, Google Cloud Platform, Alibaba Cloud Platform)',
        'Be able to develop Shell Scripts in Linux',
        'Have the capacity to be competent in machine learning and artificial intelligence( Natural Language Processing, Deep Learning, Neural Networks, Artificial Intelligence, Machine vision, Machine Learning & Data Mining)',
        'Have a passion for fully communicating with designer team to solve problems',
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
