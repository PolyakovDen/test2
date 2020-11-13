<template>
  <v-dialog
    v-model="dialog"
    max-width="750"
    @click:outside="handleClose"
  >
    <v-card color="#2f6464">
      <v-card-title class="services__title">
        {{ item.title }}
      </v-card-title>
      <v-card-text class="services__item" v-for="(item, i) in item.descriptionItems" :key="i">
        {{ item.item }}
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
  export default {
    name: "Dialog",
    props: {
      dialog: {
        type: Boolean,
        required: true,
        default: false
      },
      item: {
        type: Object,
        required: true
      },
      handleClose: {
        type: Function,
        required: true
      },
    }
  }
</script>

<style scoped>
  .services__title {
    color: #fefefe;
    font-size: 28px;
    text-transform: uppercase;
  }
</style>
