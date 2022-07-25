<template>
  <button @click="generateReport()">test</button>
  <div class="Eryuan-resume__box">
    <ResumeHeader />
    <ResumeExperience />
    <ResumeSkills />
    <ResumeEducation />
  </div>
  <vue3-html2pdf
        :show-layout="false"
        :enable-download="true"
        filename="Eryuan_Gao"
        :pdf-quality="2"
        :manual-pagination="false"
        pdf-format="a4"
        pdf-orientation="landscape"
        pdf-content-width="595px"

        @progress="onProgress($event)"
        @hasStartedGeneration="hasStartedGeneration()"
        @hasGenerated="hasGenerated($event)"
        ref="html2Pdf"
        class="pdf_control"
    >
        <template v-slot:pdf-content>
            <div class="Eryuan-resume__pdf">
              <ResumeHeader />
              <ResumeExperience />
              <ResumeSkills />
              <ResumeEducation />
            </div>
          </template>
    </vue3-html2pdf>

    
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ResumeHeader from "@/components/Header.vue";
import ResumeExperience from "@/components/Experience.vue";
import ResumeSkills from "@/components/Skills.vue";
import ResumeEducation from "@/components/Education.vue";
import Vue3Html2pdf from 'vue3-html2pdf';
export default defineComponent({
  name: 'HomeView',
  components: {
    ResumeHeader,
    ResumeExperience,
    ResumeSkills,
    ResumeEducation,
    Vue3Html2pdf
  },
  methods: {
        /*
            Generate Report using refs and calling the
            refs function generatePdf()
        */
        generateReport () {
            (this.$refs['html2Pdf'] as any).generatePdf()
        }
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
.vue-html2pdf::v-deep .layout-container.show-layout {
  z-index: -1 !important;
}
</style>