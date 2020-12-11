<template>
  <v-container fluid fill-height class="success--page">
    <v-row justify="center" align="center">
      <v-col lg="7" md="8" sm="10">
        <div class="success__messages pt-10 pb-10">
          <p class="text-center success__messages--text">Спасибо за ваше сообщение.</p>
          <p class="text-center success__messages--text">Мы свяжемся с вами в ближайшее время.</p>
          <nuxt-link class="link__home pl-10" to="/">< Вернуться на главную</nuxt-link>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: "success"
  }
</script>

<style scoped>
  .success--page {
    background-color: #2f6565;
  }
  .success__messages {
    border-radius: 10px;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
  }
  .success__messages--text {
    font-size: 21px;
  }
  .link__home {
    text-decoration: none;
  }
</style>
