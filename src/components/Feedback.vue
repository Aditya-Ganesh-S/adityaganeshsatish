<template>
  <section class="feedback">
    <h1 class="feedback__heading">What others say about me</h1>
    <div class="feedback__container">
      <carousel @next="next" @prev="prev">
        <carouselSlider
          v-for="(feedback, index) in feedbackData"
          :key="feedback"
          :index="index"
          :visibleIndex="visibleIndex"
        >
          <Story :feedback="feedback" />
        </carouselSlider>
      </carousel>
    </div>
  </section>
</template>

<script>
import Story from "./Story.vue";
import Carousel from "./Carousel.vue";
import CarouselSlider from "./CarouselSlider.vue";
export default {
  components: {
    Story,
    Carousel,
    CarouselSlider,
  },
  data() {
    return {
      visibleIndex: 0,
      feedbackData: [
        {
          name: "Scott Fisher",
          role: "Manager at Peapod Digital Labs",
          feedback:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti iste delectus quisquam voluptate temporibus non amet. Adipisci soluta sit placeat!",
        },
        {
          name: "Dan Swester",
          role: "Front-End Developer at Peapod Digital Labs",
          feedback:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti iste delectus quisquam voluptate temporibus non amet. Adipisci soluta sit placeat!",
        },
      ],
    };
  },
  computed: {
    feedbackDataLength() {
      return this.feedbackData.length;
    },
  },
  methods: {
    next() {
      if (this.visibleIndex >= this.feedbackDataLength - 1) {
        this.visibleIndex = 0;
      } else this.visibleIndex++;
    },
    prev() {
      if (this.visibleIndex <= 0) {
        this.visibleIndex = this.feedbackDataLength - 1;
      } else this.visibleIndex--;
    },
  },
};
</script>

<style lang = "scss">
@import "@/assets/_shared.scss";
@import "@/assets/_feedback.scss";
</style>