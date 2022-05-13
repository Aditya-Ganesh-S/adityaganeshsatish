<template>
  <div class="card">
    <div class="card__side card__side--front">
      <div class="card__picture">
        <img :src="project.projectImage" alt="" class="card__picture--img" />
      </div>
      <div class="card__title">
        <p class="card__title--text">{{ project.title }}</p>
      </div>
      <div class="card__techstack">
        <div v-for="techstack in project.techStack" :key="techstack">
          <img :src="techstack" alt="" class="card__techstack--img" />
        </div>
      </div>
    </div>
    <div class="card__side card__side--back">
      <div class="card__description">
        <div
          v-for="description in project.discription"
          :key="description"
          class="card__description--points"
        >
          <p>{{ description }}</p>
        </div>
      </div>
      <div>
        <a :href="project.url" class="btn btn-white">See Project</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["project"],
};
</script>


<style lang="scss">
@import "@/assets/_shared.scss";
@import "@/assets/_card.scss";
</style>