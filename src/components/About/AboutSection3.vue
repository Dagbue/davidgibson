<template>
  <div class="alpha">
    <hr class="first-line" />

    <div class="container">
      <p class="text-1">CONTACT ME</p>
      <p class="text-2">Possumus e aute sed se litteris in aliquip, a tamen quem qui pariatur ex pariatur nam nulla
        possumus, magna do nostrud non quid qui cernantur eram aliqua e illum labore proident consequat.</p>
    </div>

    <div id="contact-form" class="contact-form">
<!--      <h1 class="contact-form_title">Get in touch</h1>-->
<!--      <p class="contact-form_paragraph">Our friendly team would love to hear from you.</p>-->

      <form class="form" >


        <div class="first-part">
          <div class="form-separate">
            <div class="split">
              <label class="label-input">Full name</label>
              <input
                  required
                  name="name"
                  type="text"
                  autocomplete="off"
              />
            </div>
            <div class="split">
              <label class="label-input">Subject</label>
              <input
                  required
                  name="name"
                  type="text"
                  autocomplete="off"
              />
            </div>
          </div>

          <div class="split">
            <label class="label-input">Email address</label>
            <input
                required
                name="email"
                type="email"
            />
          </div>
        </div>
        <div class="second-part">
          <div class="split">
            <label class="label-input">Message</label>
            <textarea
                name="message"
                rows="7"
                placeholder="Leave us a message..."
                required
                style="
                                    font-family: 'BR-Firma-Regular', sans-serif;
                                    letter-spacing: 1.5px;
                                    font-size: 13px;
"
            ></textarea>
          </div>

<!--          <div class="split-2">-->
<!--            <input type="checkbox" class="checkbox"/>-->
<!--            <label class="check-box-label">You agree to our friendly privacy policy.</label>-->
<!--          </div>-->

          <button class="button">
            Send message
            <img src="@/assets/arrow-right-line.svg" alt="btn-image" class="btn-image" />
          </button>
        </div>

      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutSection3"
}
</script>


<style scoped>
.alpha{
  margin-top: 5%;
  margin-bottom: 5%;
}

.container{
  padding: 50px 0 25px 0;
  margin-left: 8%;
}

.text-1{
  font-weight: 700;
  letter-spacing: 0px;
  line-height: 1.1;
  color: #333333;
  font-size: 1.7rem;
  font-family: 'BR-Firma-Bold', sans-serif;
}



.text-2{
  width: 80%;
  padding-top: 1%;
  padding-bottom: 1.5%;
  font-size: 1.1rem;
  line-height: 1.4;
  color: #333333;
}

.first-line{
  border: solid 0.6px #EEF0F1;
}

.first-part{
  width: 100%;
}

.second-part{
  width: 100%;
}

.contact-form {
  width: 85%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.contact-form  {
  /*border-bottom: solid 1px #ccc;*/
  /*margin-bottom: 15px;*/
}

.contact-form .form {
  display: flex;
  gap: 20px;
  font-size: 16px;
}

.contact-form_title {
  text-align: left;
  font-size: 36px;
  line-height: 44px;
  padding-bottom: 10px;
  color: #101828;
  font-family: 'BR-Firma-Bold', sans-serif;
}

.contact-form_paragraph {
  text-align: left;
  font-size: 20px;
  line-height: 30px;
  padding-bottom: 6%;
  color: #475467;
}

.contact-form input[type="email"],
.contact-form input[type="text"],
.contact-form textarea {
  padding: 11px 16px;
  margin-bottom: 15px;
  margin-top: 5px;
  outline: none;
  width: 100%;
  border-radius: 6px;
}

.contact-form textarea {
  resize: none;
}

.contact-form .button {
  background: #333;
  border: solid 1px #333;
  color: white;
  cursor: pointer;
  padding: 13px 16px;
  text-align: center;
  border-radius: 6px;
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: center;
  gap: 2.5px;
}

.contact-form .button:hover {
  background: #333;
  border: solid 1px #333;
}

.contact-form input[type="email"],
.contact-form input[type="text"],
.contact-form input[type="checkbox"],
.contact-form textarea,
.contact-form .button {
  font-size: 15px;
  border: solid 1px #EEF0F1;
  width: 100%;
}
</style>