<template>
  <div class="Eryuan-resume-header">
    <div id="header-row" class="Eryuan-resume-row">
      <div class="Eryuan-resume-row__l">
        <div class="Eryuan-resume-h1">Eryuan Gao</div>
        <div class="Eryuan-resume-h2 mt-4">Sydney, NSW 2018</div>
        <div class="Eryuan-resume-header__contact Eryuan-resume-row">
          <div class="Eryuan-resume-header__contact-item">
            <LoadIcon class="ml-10" :iconName="email_icon" />
            <div class="Eryuan-resume-header__contact-text">gaoeryuan97@gmail.com</div>
          </div>
          <div class="Eryuan-resume-header__contact-item">
            <LoadIcon class="ml-10" :iconName="phone_icon" />
            <div class="Eryuan-resume-header__contact-text">0427565969</div>
          </div>
          <div class="Eryuan-resume-header__contact-item">
            <LoadIcon class="ml-10" :iconName="github_icon" />
            <div class="Eryuan-resume-header__contact-text"><a href="https://github.com/gaoshaoye">github.com/gaoshaoye</a> - <a href="https://www.linkedin.com/in/eryuan-gao/">www.linkedin.com/in/eryuan-gao/</a></div>
          </div>
        </div>
      </div>
      <div class="Eryuan-resume-row__r">
      </div>
    </div>
  </div>
      <div class="Eryuan-resume-div" />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import LoadIcon from "@/components/LoadIcon.vue";
export default defineComponent({
  name: 'CLHeader',
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
@import "@/assets/style.scss";
.Eryuan-resume-header__contact {
  @extend .Eryuan-resume-p2;
  margin-top: 14px;
  align-items: center;
  flex-wrap: wrap;
  margin-left: -10px;
  &-text {
    margin-left: 6px;
  }
  &-item {
    display: flex;
  }
}
a {
  @extend .Eryuan-resume-p2;

}
.Eryuan-resume-header__Prof {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: #D9D9D9;
  overflow: hidden;
}

</style>
