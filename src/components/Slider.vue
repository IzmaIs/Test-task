<template>
  <div class="slider">
    <slot></slot>
    <button @click="next" class="next"><i class="arrow right"></i></button>
    <button @click="prev" class="prev"><i class="arrow left"></i></button>
  </div>
</template>

<script>
export default {
  data(){
    return{
    }
  },
  methods: {
    next() {
      this.$emit('next')
    },
    prev() {
      this.$emit('prev')
    }
  }
}
</script>

<style>
@import "../assets/styles/slider.scss";
</style>