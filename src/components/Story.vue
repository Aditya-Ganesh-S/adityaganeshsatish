<template>
  <div class="story">
    <figure class="story__shape">
      <img src="../assets/img/scottPlaceholder.jpg" alt="" class="story__img" />
    </figure>
    <div class="story__text">
      <p class="story__text--name">{{ feedback.name }}</p>
      <p>{{ feedback.feedback }}</p>
      <p class="story__text--position">Senior Software engineer manager at Peapod Digital Labs</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["feedback"],
};
</script>

<style lang="scss">
@import "@/assets/_shared.scss";
@import "@/assets/_story.scss";
</style>