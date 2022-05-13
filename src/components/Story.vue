<template>
  <div class="story">
    <figure class="story__shape">
      <img src="../assets/img/nat-8.jpg" alt="" class="story__img" />
    </figure>
    <div class="story__text">
      <p>{{ feedback.name }}</p>
      <p>{{ feedback.feedback }}</p>
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