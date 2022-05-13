<template>
  <div class="carousel">
    <slot></slot>
    <img src="../assets/img/leftArrow.svg" class="prev" alt="" @click="prev" />
    <img src="../assets/img/rightArrow.svg" class="next" alt="" @click="next" />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  components: {},
  methods: {
    next() {
      this.$emit("next");
    },
    prev() {
      this.$emit("prev");
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/_shared.scss";
@import "@/assets/_carousel.scss";
</style>