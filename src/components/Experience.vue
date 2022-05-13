<template>
  <div class="experience__container--main">
    <img :src="experience.logo" alt="" class="experience__logo" />
    <div class="experience__container mt-8">
      <div class="experience__container--sub">
        <h1 class="experience__company">{{ experience.company }}</h1>
        <p class="experience__duration">{{ experience.duration }}</p>
      </div>
      <p class="experience__role">{{ experience.role }}</p>
      <ul class="experience__responsibilities">
        <li
          v-for="responsibility in experience.resposibilities"
          :key="responsibility"
        >
          {{ responsibility }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: ["experience"],
};
</script>

<style lang="scss">
@import "@/assets/_shared.scss";
@import "@/assets/_experience.scss";
</style>