<template>
  <div class="carousel-slide" v-show="visibleIndex === index">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: ["visibleIndex", "index"],
};
</script>

<style lang="scss">
@import "@/assets/_shared.scss";
@import "@/assets/_carousel.scss";
</style>