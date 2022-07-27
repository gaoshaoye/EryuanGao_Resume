<template>
<div class="tool-bar">
  <div class="tool-bar__buttons">
    <button v-if="contentId=='#printCL'" @click="changePage()" class="CV_button">Resume</button>
    <button v-if="contentId=='#printCV'" @click="changePage()" class="CL_button">Cover Letter</button>
    <button class="print_button" v-print='contentId'>Print / Download</button>
  </div>
  <div class="tool-bar__input">
      <input type="text" placeholder="Company Name" v-model="company" />
      <input type="text" placeholder="Position" v-model="position" />
  </div>
</div>

<HomeView v-if="contentId=='#printCV'" />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HomeView from "@/views/HomeView.vue";


export default defineComponent({
  name: 'PrintView',
  components: {
  HomeView
  },
  data() {
    return {
      contentId: '#printCV',
      company:'',
      position: '',
    }
  },
  methods: {
    changePage(){
      if (this.$data.contentId == '#printCL'){
        this.$data.contentId = '#printCV'
      } else {
        this.$data.contentId = '#printCL'
      }
      console.log(this.$data.contentId)
    }
  },
});
</script>
<style lang="scss" scoped>
@import "@/assets/style.scss";
.print_button {
  margin-right: 0px;
  margin-left: auto;
}
.tool-bar {
  background-color: #ffffff;
  padding: 20px 12px;
  &__buttons {
    display: flex;
    justify-items: end;
  }
  &__input {
    margin-top: 8px;
  }
}

</style>