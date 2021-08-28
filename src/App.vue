<template>
  <div id="app">
    <TopHead/>
    <Gallery/>
    <Features/>
    <Intro/>
    <FooterMobile/>
  </div>
</template>

<script>
import TopHead from './components/TopHead.vue';
import Gallery from './components/Gallery.vue';
import Features from "@/components/Features";
import Intro from "@/components/Intro";
import FooterMobile from "@/components/FooterMobile";

export default {
  name: 'App',
  components: {
    Intro,
    Features,
    TopHead,
    Gallery,
    FooterMobile,
  }
}
</script>

<style>
</style>
