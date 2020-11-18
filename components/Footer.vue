<template>
  <div class="footer elevation-23 pb-5">
    <v-container fluid class="pa-0">
      <h2 class="footer__title text-center pt-6" data-aos="flip-up">Наши контакты</h2>
      <div class="footer__wrapper pa-10 pb-5 d-flex justify-space-between flex-wrap">
        <div class="footer__contacts">
          <div class="email d-flex">
            <img src="/envelope.png" class="mr-4 mt-1" width="25" height="18">
            <p>new_startdigital@gmail.com</p>
          </div>
          <div class="telephone d-flex">
            <img src="/phone-ringing.png" class="mr-4" width="25" height="24">
            <p>+380937390565</p>
          </div>
          <div class="location d-flex">
            <img src="/placeholder.png" class="mr-5" width="22" height="25">
            <p>Киев, Украина</p>
          </div>
        </div>
        <div class="footer__socials d-flex justify-space-between flex-wrap">
          <a href="" class="footer__socials--item mr-5">
            <img src="/facebook.png" alt="facebook">
          </a>
          <a href="" class="footer__socials--item mr-5">
            <img src="/instagram.png" alt="instagram">
          </a>
          <a href="" class="footer__socials--item">
            <img src="/linkedin.png" alt="linkedin">
          </a>
          <a href="" class="footer__socials--item mr-5 mt-3">
            <img src="/whatsapp.png" alt="whatsapp">
          </a>
          <a href="" class="footer__socials--item mr-5 mt-3">
            <img src="/viber.png" alt="viber">
          </a>
          <a href="" class="footer__socials--item mt-3">
            <img src="/telegram.png" alt="telegram">
          </a>
        </div>
      </div>
      <div class="privacy text-center mt-8">
        <nuxt-link to="/privacy" class="privacy__link">
          <p class="privacy__title mb-0"><span>© 2020 EU.</span> All rights reserved. <span>T&C</span></p>
        </nuxt-link>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
  .container {
    max-width: 1100px !important;
  }
  .footer__wrapper {
    border-bottom: 2px solid !important;
  }
  .footer__title {
    letter-spacing: 5px;
    font-size: 30px;
  }
  .footer__contacts {
    font-size: 18px;
    letter-spacing: 3px;
  }
  .footer__socials {
    max-width: 220px;
  }
  @media screen and (max-width: 650px) {
    .footer__wrapper {
      justify-content: center !important;
    }
    .footer__contacts {
      text-align: center;
    }
    .footer__socials {
      margin-top: 30px;
    }
  }
  .privacy__link {
    display: inline-block;
    font-size: 17px;
    color: #fff;
    text-decoration: none;
  }
  .privacy__title span {
    font-style: italic;
  }
</style>
