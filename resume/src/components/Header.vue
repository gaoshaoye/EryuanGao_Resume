<template>
  <div class="Eryuan-resume__header">
  <LoadIcon  :iconName="email_icon" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import LoadIcon from "@/components/LoadIcon.vue";
export default defineComponent({
  name: 'ResumeHeader',
  components: {
    LoadIcon,
  },
  data(){
    return{
      email_icon: 'email_icon', 
      phone_icon: 'phone_icon',
      github_icon: 'link_icon',
    }
  },
});
</script>


<style scoped lang="scss">

</style>
