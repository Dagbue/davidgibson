<template>
  <div class="alpha">
    <about-section1/>
    <about-section2/>
    <about-section3/>
    <home-footer/>
  </div>
</template>

<script>
import HomeFooter from "@/components/Home/HomeFooter.vue";
import AboutSection1 from "@/components/About/AboutSection1.vue";
import AboutSection2 from "@/components/About/AboutSection2.vue";
import AboutSection3 from "@/components/About/AboutSection3.vue";

export default {
  name: 'AboutView',
  components: {AboutSection3, AboutSection2, AboutSection1, HomeFooter},
}
</script>

<style scoped>

</style>
