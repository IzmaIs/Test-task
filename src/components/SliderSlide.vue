<template>
  <transition :name="direction" mode="in-out">
    <div v-show="visibleSlide === index" class="slider-slide">
      <slot></slot>
    </div>
  </transition>
</template>

<script>
export default {
  props: ['visibleSlide', 'index', 'direction'],
  data() {
    return {

    }
  }
}
</script>

<style>
@import "../assets/styles/sliderSlide.scss";
</style>