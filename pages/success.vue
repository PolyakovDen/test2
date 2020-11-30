<template>
  <div class="success">
    <v-container>
      <div class="success__messages">
        <p class="text-center">Спасибо за ваше сообщение.</p>
        <p class="text-center">Мы свяжемся с вами в ближайшее время.</p>
      </div>
    </v-container>
  </div>
</template>

<script>
  export default {
    name: "success"
  }
</script>

<style scoped>
  .success {
    background-color: #000000;
  }
  .success__messages {
    background-color: #f3ca20;
  }
</style>
