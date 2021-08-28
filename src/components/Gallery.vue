<template>
  <div class="gallery">
    <slider @next="next" @prev="prev">
      <slider-slide v-for="(slide, index) in slides"
                    :key="slide"
                    :index="index"
                    :visibleSlide="visibleSlide"
                    :direction="direction"
      >
        <div class="slide" :style="{backgroundImage: `url(${slide})`}"
        />
        <!--        <img :src="slide"/>-->
      </slider-slide>
    </slider>
  </div>
</template>

<script>
import Slider from "@/components/Slider";
import SliderSlide from "@/components/SliderSlide";

export default {
  data() {
    return {
      slides: [
        './imgs/Gallery.png',
        'https://picsum.photos/id/232/1110/400',
        'https://picsum.photos/id/233/1110/400',
        'https://picsum.photos/id/234/1110/400',
        'https://picsum.photos/id/235/1110/400',
      ],
      visibleSlide: 0,
      direction: 'left'
    }
  },
  computed: {
    slidesLen() {
      return this.slides.length;
    }
  },
  methods: {
    next() {
      if (this.visibleSlide >= this.slidesLen - 1) {
        this.visibleSlide = 0;
      } else {
        this.visibleSlide++;
      }
      this.direction = "left"
    },
    prev() {
      if (this.visibleSlide <= 0) {
        this.visibleSlide = this.slidesLen - 1;
      } else {
        this.visibleSlide--;
      }
      this.direction = "right"
    }
  },
  components: {
    Slider,
    SliderSlide
  }
}
</script>

<style scoped>
@import "../assets/styles/gallerystyles.scss";
</style>