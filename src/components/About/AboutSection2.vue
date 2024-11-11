<template>
  <div class="alpha">
    <div class="text-part">
      <p class="text-1">David Gibson is a financial advisor working in Tucson, Arizona, who has been in the
        industry for 27 Years. David Gibson is on the advisory team at RBC Capital Markets, LLC. The advisor
        has gained experience at Morgan Stanley Smith Barney, BGR Financial Group, LLC and UBS PAINEWEBBER INC.
        Lozano maintains a Series 7, Series 63, Series 65, Series 66, and SIE license, certifying them as both a
        securities agent and an investment advisor representative, with 23 state licenses.</p>
      <p class="text-2">
        I build strong relationships with my valued clients by understanding their goals, supporting their concerns,
        and providing strategic solutions.
      </p>
      <p class="text-3">
        David Gibson is on a mission is to support men/women with the tools to empower them for all aspects of
        their financial wellbeing. This support is for men/women of all ages and backgrounds. Let us teach you how to
        make decisions for your future.
      </p>
    </div>

    <div class="image-part">
      <img src="https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/slider1.jpg" alt="" class="image" />
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutSection2"
}
</script>

<style scoped>
.alpha{
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
  margin-top: 4%;
}
.text-part{
  width: 50%;
}
.image-part{
  width: 50%;
}
.image{
  max-width: 50%;
  display: block;
  margin-left: auto;
  margin-right: auto;
  box-shadow: rgba(100, 100, 111, 0.5) 0px 7px 29px 0px;
}

.text-1{
  margin-top: 3%;
  margin-left: 17%;
  line-height: 1.5;
  font-size: 1.2rem;
}

.text-2{
  margin-top: 4%;
  margin-left: 17%;
  line-height: 1.5;
  font-size: 1.3rem;
  font-family: 'BR-Firma-Bold', sans-serif;
  letter-spacing: 0;
}

.text-3{
  margin-top: 4%;
  margin-left: 17%;
  line-height: 1.5;
  font-size: 1.2rem;
}


@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .alpha{
    display: flex;
    flex-direction: column-reverse;
    margin-top: 4%;
  }

  .text-part{
    width: 90%;
  }
  .image-part{
    width: 90%;
  }

  .image{
    max-width: 90%;
  }

  .text-1{
    margin-left: unset;
  }

  .text-2{
    margin-left: unset;
  }

  .text-3{
    margin-left: unset;
  }
}

@media (max-width: 500px) {

}
</style>