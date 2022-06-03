<template>
  <div class="Eryuan-resume-education mt-18">
    <div class="Eryuan-resume-h1">Education</div>
    <ResumeGroup v-for="(item,i) in educations" v-bind:key="i" :start="item.when" :middle="item.uni" :end="item.location" />


  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ResumeGroup from "@/components/Group.vue";

export default defineComponent({
  name: 'ResumeEducation',
  components: {
    ResumeGroup,
  },
  data(){
    return{

      
      educations: [
        {
          when:'Dec 2021',
          uni: 'Master of Information Technology: Artificial Intelligence',
          location: 'University of New South Wales | Sydney, Australia',
        },
        {
          when:'Jun 2019',
          uni: 'Bachelor of Engineering: Computer Science And Information Engineering',
          location: 'Tamkang University | New Taipei, Taiwan',
        },
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
