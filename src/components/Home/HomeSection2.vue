<template>
  <div class="admin">

    <div class="section-1-alpha">
      <div class="section-1">

        <div class="section-1-image">
          <img src="https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-20-at-11.31.54_9ea12298-842x1024.jpg" alt="" class="section-1-image" />
        </div>
        <div class="section-1-text">
          <p class="text-1">
            <span class="text-1-link">Financial Advisory, </span>
            <span class="text-1-link">Financial Management, </span>
            <span class="text-1-link">Personal Financial Advisor for WellsFargo, </span>
          </p>
          <p class="text-2">Forex Trading: A Lifestyle Beyond a Profession</p>
          <p class="text-3">Forex trading is not just a profession, it’s a lifestyle. Balancing family time and
            trading requires discipline and understanding from both sides</p>
          <p class="text-4">
            <span class="slash">BY ADMIN / </span>
            <span class="slash">JANUARY 22, 2024 / </span>
            <span class="slash">1 MIN READ</span>
          </p>
        </div>


      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "HomeSection2"
}
</script>

<style scoped>
.section-1-alpha{

}

.section-1{
  display: flex;
  justify-content: center;
  margin-top: 5%;
}

.section-1-text{
  padding: 1.5rem 1.5rem 1.5rem 3rem;
  width: 55%;
  border: 0.5px solid rgba(0, 0, 0, 0.2);
  border-left: none;
  transition: border 200ms ease;
  border-radius: 0 6px 6px 0;
  height: 310px;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;

}

.section-1-image{
  width: 250px;
  border-radius: 6px 0 0 6px;
  height: 310px;
}

.text-1{
  padding-top: 1rem;
  padding-bottom: 1rem;
  font-size: 0.875rem;
  text-transform: uppercase;
  font-weight: 700;
  line-height: 1.5;
  color: #51cbce;
}

.text-2{
  margin-bottom: 1.5rem;
  font-family: 'BR-Firma-Bold', sans-serif;
  font-weight: bold;
  letter-spacing: 0px;
  line-height: 1.3;
  color: #333333;
  font-size: 1.8rem;
}

.text-3{
  font-size: 1.1rem;
}

.text-4{
  padding-top: 10%;
  font-size: 0.9rem;
}

@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .section-1{
    display: block;
    width: 100%;
  }

  .section-1-text{
    display: block;
    margin-right: auto;
    margin-left: auto;
    width: 95%;
    height: 100%;
    border-radius: unset;
    border: unset;
    padding: 1.5rem;
  }

  .section-1-image{
    border-radius: unset;
    height: 450px;

    display: block;
    margin-right: auto;
    margin-left: auto;
    width: 97%;
  }
}

@media (max-width: 500px) {

}
</style>