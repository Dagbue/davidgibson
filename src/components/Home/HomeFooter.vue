<template>
  <div class="alpha">

    <div class="container">
      <p class="text-1">About Me</p>
      <hr class="first-line"/>
      <p class="text-2">Discover the power of strategic financial asset management with David Gibson.</p>
      <p class="text-3" @click="onPostClick">READ MORE</p>
    </div>
    <hr class="second-line"/>
    <p class="text-4">@2024 All Right Reserved <span style="color: #51cbce;">David Gibson Feeds</span></p>

  </div>
</template>

<script>
export default {
  name: "HomeFooter",
  methods: {
    onPostClick() {
      this.$router.push("/about");
      window.scrollTo(0, 0);
    },
  },
}
</script>

<style scoped>
.alpha{
  background-color: #fafafa;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  background-attachment: scroll;
  padding-bottom: 1%;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 6px 28px 0px;
}
.container{
  padding: 80px 0 50px 0;
  margin-left: 10%;
}

.text-1{
  font-weight: 700;
  letter-spacing: 0px;
  line-height: 1.3;
  color: #333333;
  font-size: 1.4rem;
}

.first-line{
  margin-bottom: 5px;
  margin-top: 5px;
  width: 300px;
  height: 3px; /* Adjust the height to your preference */
  border: none; /* Removes the default border styling */
  background: linear-gradient(to right, #51cbce 50%, #333333 50%);
}

.text-2{
  width: 45%;
  padding-top: 1%;
  padding-bottom: 1.5%;
}


.text-3{
  font-size: 0.875rem;
  font-weight: 700;
  padding: 0.5rem 25px;
  line-height: 1.75;
  cursor: pointer;
  text-transform: uppercase;
  background-color: #333;
  border: 1px solid #333;
  color: #FFFFFF;
  opacity: 1;
  outline: none !important;
  box-shadow: none !important;
  border-radius: 6px;
  display: inline-block;
}

.text-3:hover {
  box-shadow: rgba(100, 100, 111, 1) 5px 7px 29px 5px;
}

.text-4{
  text-align: center;
  padding-top: 1.7%;
  font-size: 15px;
}

.second-line{
  border: 0.5px solid #e6e6e6;
}

@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .text-2{
    width: 90%;
  }

  .container{
    padding: 60px 0 50px 0;
    margin-left: 5%;
  }
}

@media (max-width: 500px) {

}
</style>