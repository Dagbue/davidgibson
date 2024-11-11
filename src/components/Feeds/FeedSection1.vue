<template>
  <div class="alpha">

    <div class="container">
      <p class="text-1">FEEDS</p>
      <hr class="first-line"/>
<!--      <p class="text-2">Licensed Broker and Financial Advisor.</p>-->
    </div>

  </div>
</template>

<script>
export default {
  name: "FeedSection1"
}
</script>

<style scoped>
.alpha{
  background-color: #d4d4da;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  background-attachment: scroll;
  padding-bottom: 1.5%;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}
.container{
  padding: 80px 0 50px 0;
  margin-left: 8%;
}

.text-1{
  font-weight: 700;
  letter-spacing: 0px;
  line-height: 1.3;
  color: #333333;
  font-family: 'BR-Firma-Bold', sans-serif;
  font-size: 1.7rem;
}

.first-line{
  margin-top: 6px;
  width: 400px;
  height: 3px; /* Adjust the height to your preference */
  border: none; /* Removes the default border styling */
  background: linear-gradient(to right, #51cbce 50%, #919191 50%);
}

.text-2{
  width: 45%;
  padding-top: 1%;
  padding-bottom: 1.5%;
  color: #333333;
  font-size: 1rem;
}


.text-3{
  font-size: 0.875rem;
  font-weight: 700;
  padding: 0.5rem 18px;
  line-height: 1.75;
  cursor: pointer;
  text-transform: uppercase;
  background-color: #333;
  border: 2px solid #333;
  color: #FFFFFF;
  opacity: 1;
  outline: none !important;
  box-shadow: none !important;
  border-radius: 0px !important;
  display: inline-block;
}

.text-4{
  text-align: center;
  padding-top: 1.7%;
}

.second-line{
  border: 0.5px solid #e6e6e6;
}

@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .first-line{
    width: 250px;
  }
}

@media (max-width: 500px) {

}
</style>