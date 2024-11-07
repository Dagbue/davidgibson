<template>
  <div class="alpha">
    <feed-section1/>
    <feed-section2/>
    <home-footer/>
  </div>
</template>

<script>
import FeedSection1 from "@/components/Feeds/FeedSection1.vue";
import FeedSection2 from "@/components/Feeds/FeedSection2.vue";
import HomeFooter from "@/components/Home/HomeFooter.vue";

export default {
  name: "FeedsView",
  components: {HomeFooter, FeedSection2, FeedSection1}
}
</script>

<style scoped>

</style>