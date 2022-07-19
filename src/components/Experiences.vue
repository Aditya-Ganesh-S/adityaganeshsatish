<template>
  <section class="experience">
    <h1 class="experience__heading">Professional Experience</h1>
    <div class="experience__box"
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
            "Created components using Vue JS, JavaScript, SCSS to enhance functionality and user experience on webpages",
            "Refactored and migrated components that has enhanced the performance of the repositories",
            "Worked with senior developers to write code from scratch that impacts 10+ clients of Ahold Delhaize USA",
            "Engaged in tech team meetings to talk about ongoing and upcoming projects and strategies on how to produce effective work",
            "Altered existing codes to make them more responsive on mobile devices",
          ],
          logo: peapodLogo,
        },
        {
          company: "Northeastern University",
          duration: "Aug 2021 - Dec 2021",
          role: "Customer service Technician",
          resposibilities: [
            "Troubleshoot technical problems for students, faculty, and staff at Northeastern University of strength 10000+, both in-person and via telephone",
            "Analyzed, diagnosed, documented, and resolved issues concerning hardware and software of computers, phones, and printers; learning management systems; websites, networks, and emails."
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