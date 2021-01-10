<template>
  <div class="">
    <div class="form__block">
      <div class="form__block--wrapper">
        <div class="form__title--block">
          <h2 class="form__title" data-aos="fade-up">
            Оставьте заявку и
            получите расчет
            стоимости вашего
            проекта уже сегодня
          </h2>
        </div>
      </div>
    </div>
    <div class="form">
      <v-form
        ref="form"
        name="formPost"
        v-model="valid"
        lazy-validation
      >
        <v-container>
          <v-row justify="center" class="pa-2">
            <v-col
              class="test pa-8 pb-3"
              cols="12"
              xl="4"
              md="5"
              sm="8"
            >
              <v-text-field
                v-model="name"
                name="name"
                :counter="10"
                :rules="nameRules"
                label="Имя"
                required
              />
              <v-text-field
                v-model="email"
                name="email"
                :rules="emailRules"
                label="E-mail"
                required
              />
              <v-text-field
                v-model="number"
                name="number"
                :rules="numberRules"
                label="Номер телефона"
                required
              />
              <v-textarea
                v-model="annotation"
                name="annotation"
                label="Примечание"
                auto-grow
                required
              />
<!--              <div class="field">-->
<!--                <div data-netlify-recaptcha="true"></div>-->
<!--              </div>-->
              <v-btn
                :disabled="!valid"
                color="#f0f0f0"
                elevation="20"
                block
                class="mr-4"
                @click="validate"
                type="submit"
              >
                Отправить
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Form',
  data: () => ({
    valid: true,
    name: '',
    nameRules: [
      v => !!v || 'Заполните имя пожалуйста',
      v => (v && v.length <= 10) || 'Имя должно быть меньше 10 символов'
    ],
    email: '',
    emailRules: [
      v => !!v || 'Заполните E-mail пожалуйста',
      v => /.+@.+\..+/.test(v) || 'E-mail должен быть формата: test@test.com'
    ],
    number: '',
    numberRules: [
      v => !!v || 'Заполните телефон пожалуйста'
    ],
    annotation: ''
  }),
  methods: {
    validate () {
      this.$refs.form.validate()
    }
  }
}
</script>

<style scoped>
  .form__block {
    background-image: url("/form-bg.webp");
    background-position: top center;
    background-repeat:no-repeat;
    -webkit-background-size:cover;
    -moz-background-size:cover;
    -o-background-size:cover;
    background-size:cover;
  }
  .form__block--wrapper {
    display: flex;
    height: 75vh;
    background-color: rgba(0, 0, 0, .8);
  }
  .form__title--block {
    display: flex;
    margin: auto;
    align-items: flex-end;
    margin-bottom: 100px;
  }
  .form__title {
    max-width: 700px;
    letter-spacing: 10px;
    text-align: center;
    font-size: 40px;
    text-transform: uppercase;
  }
  @media screen and (max-width: 450px) {
    .form__title {
      font-size: 25px;
      word-wrap: break-word !important;
    }
  }
  .form {
    margin-top: 80px;
    margin-bottom: 80px;
  }
  .test {
    border: 3px solid;
  }
  ::v-deep .v-btn__content {
    text-transform: none;
    color: #2f6565;
  }
</style>
