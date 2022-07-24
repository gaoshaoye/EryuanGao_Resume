<template>
  <div class="Eryuan-resume-header">
    <div id="header-row" class="Eryuan-resume-row">
      <div class="Eryuan-resume-row__l">
        <div class="Eryuan-resume-h1">Eryuan Gao</div>
        <div class="Eryuan-resume-h2 mt-4">Front End Developer</div>
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
        <!-- <div class="Eryuan-resume-header__Prof"></div> -->
      </div>
    </div>
    <div class="Eryuan-resume-div" />
    <div class="Eryuan-resume-bio">
      <div class="Eryuan-resume-bio-quotation">“</div>
      <div class="ml-4 Eryuan-resume-bio-text">
        <div class="Eryuan-resume-bio-text">{{ bio }}</div>
        <div class="Eryuan-resume-bio-quotation ml-4 end">”</div>
      </div>
    </div>
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
      bio: 'A motivated master of Information Technology majored in web development, artificial intelligence, pattern recognition, and machine vision. An educated web developer, and software engineer, who is quick to ramp up with any existing development platform and perform design, coding, debugging, and testing application and system software. Have the ability and experience in responsive web development with the MVC framework.',
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
.Eryuan-resume-bio {
  @extend .Eryuan-resume-p1;
  margin-top: 18px;
  display: flex;
  &-text {
    max-width: 494px;
  }
  &-quotation {
    
    color: $Second-Gray;
    font-family: 'Inter';
    font-style: normal;
    font-weight: 400;
    font-size: 22px;
    line-height: 27px;
    padding-left: 439px;
    position: relative;
    margin-top: -15px;
    @media screen and (max-width:595px) {
     display: none;

    }
    &:not(.end) {
      padding-left: 0px;
      margin-top: 0px;

      
    }
  }
}

</style>
