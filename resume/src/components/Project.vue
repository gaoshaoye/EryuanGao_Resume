<template>
  <div class="Eryuan-resume-project">
    <div class="Eryuan-resume-h1">University Projects</div>
    <div v-for="(project,projectIndex) in projects" :key="projectIndex">
      <ResumeGroup :start="project.when" :middle="project.where" :end="project.what" />
      <BulletPoint v-for="(text,i) in project.textList" :key="i" :text="text" />
    </div>
    
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ResumeGroup from "@/components/Group.vue";
import BulletPoint from "@/components/BulletPoint.vue";
export default defineComponent({
  name: 'ResumeProject',
  components: {
    ResumeGroup,
    BulletPoint,

  },
  data(){
    return{
      projects:[
        {
          when:'Aug 2021 - Dec 2021',
          where:'The Business-to-consumer E-Commerce Recommender System',
          what:'Team Leader',
          textList: [
            'Led a 5-person team to develop this project; allocated development tasks for front-end and back-end teams; managed the project using agile development methodology with Jira platform.',
            "Collected around 80 surveys on campus, analysed and Visualised data with Python (matplotlib); categorised data, and organised it into user stories.",
            "Based on the weighted user stories, designed and developed the E-Commerce platform; used Vue, javascript and CSS for the front end; used Python(Flask) for the back end and Alibaba Cloud Service for the cloud database.",
            "Trained and tuned decision-tree-based AI models based on simulated data; achieved accurate recommendation of 500 products in the database for user needs."
          ],
        },
        {
          when:'Jun 2022 - Current',
          where:'The Open Source E-Commerce Order Status Visualisation System Component(Project Kimi)',
          what:'Individual Open Source Developer',
          textList: [
            'Consulted with professional front-end developers; conducted the problem of the lack of useful Dashboard style components in the existing popular Vue UI library such as Element UI and Vant.',
            "Developed this E-Commerce Order Status Visualisation System Component using Vue 3.0, TypeScript and SCSS; Earned 20 stars after releasing on Github.",
          ],
        },
      ]


      
    }
  },
  
});
</script>


<style scoped lang="scss">
@import "@/assets/style.scss";
.Eryuan-resume-project {
  margin-top: 22px;
}

</style>
