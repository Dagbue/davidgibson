<template>
  <div class="alpha">
    <hero-section/>
    <home-section1/>
    <home-section2/>
    <home-section3/>
    <home-section4/>
    <home-section5/>
    <home-section6/>
    <home-footer/>
  </div>
</template>

<script>
import HeroSection from "@/components/Home/HeroSection.vue";
import HomeSection1 from "@/components/Home/HomeSection1.vue";
import HomeSection2 from "@/components/Home/HomeSection2.vue";
import HomeSection3 from "@/components/Home/HomeSection3.vue";
import HomeSection4 from "@/components/Home/HomeSection4.vue";
import HomeSection5 from "@/components/Home/HomeSection5.vue";
import HomeSection6 from "@/components/Home/HomeSection6.vue";
import HomeFooter from "@/components/Home/HomeFooter.vue";

export default {
  name: 'HomeView',
  components: {
    HomeFooter,
    HomeSection6, HomeSection5, HomeSection4, HomeSection3, HomeSection2, HomeSection1,
    HeroSection},
}
</script>

<style scoped>

</style>