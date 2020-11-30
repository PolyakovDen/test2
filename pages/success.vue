<template>
<!--  <div class="success&#45;&#45;page">-->
    <v-container fluid fill-height class="success--page">
      <v-row justify="center" align="center">
        <v-col lg="7" md="8" sm="10">
          <div class="success__messages pt-10 pb-10">
            <p class="text-center success__messages--text">Спасибо за ваше сообщение.</p>
            <p class="text-center success__messages--text">Мы свяжемся с вами в ближайшее время.</p>
            <nuxt-link class="link__home pl-10" to="/"><- Вернуться на главную</nuxt-link>
          </div>
        </v-col>
      </v-row>
    </v-container>
<!--  </div>-->
</template>

<script>
  export default {
    name: "success"
  }
</script>

<style scoped>
  .success--page {
    background-color: #0F4C5C;
  }
  .success__messages {
    border-radius: 10px;
    background-color: #E36414;
  }
  .success__messages--text {
    font-size: 21px;
    color: #5F0F40;
  }
  .link__home {
    text-decoration: none;
    color: #0f4c5c;
  }
</style>
