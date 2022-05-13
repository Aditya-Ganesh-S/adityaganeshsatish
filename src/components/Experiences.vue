<template>
  <section class="experience">
    <h1 class="experience__heading">Professional Experience</h1>
    <div
      v-for="experience in professionalExperiences"
      :key="experience.companyName"
    >
      <Experience :experience="experience" />
    </div>
  </section>
</template>

<script>
import Experience from "./Experience.vue";
import peapodLogo from "../assets/img/peapod_logo.svg";
import NortheasternLogo from "../assets/img/Northeastern.png";

export default {
  components: {
    Experience,
  },
  data() {
    return {
      professionalExperiences: [
        {
          company: "Peapod Digital Labs",
          duration: "January 2022 - June 2022",
          role: "Front-End Developer Co-op",
          resposibilities: [
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, consectetur adipiscing elit",
            "Lorem isum dolor sit amet, consectetur adipiscing elit, consectetur",
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, consectetur adipiscing",
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit consectetur adipiscing elit",
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          ],
          logo: peapodLogo,
        },
        {
          company: "Northeastern University",
          duration: "Aug 2021 - Dec 2021",
          role: "Customer service Technician",
          resposibilities: [
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, consectetur adipiscing elit",
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, consectetur",
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, consectetur adipiscing",
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit consectetur adipiscing elit",
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          ],
          logo: NortheasternLogo,
        },
      ],
    };
  },
};
</script>

<style lang = "scss">
@import "@/assets/_shared.scss";
@import "@/assets/_experience.scss";
</style>