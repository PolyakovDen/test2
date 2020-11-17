<template>
  <v-dialog
    v-model="dialog"
    max-width="750"
    @click:outside="handleClose"
    @click="iconClose"
  >
    <v-card class="card__description" color="#2f6464">
      <h2 class="services__title text-center">
        {{ item.title }}
      </h2>
      <v-btn @click="iconClose" class="close-icon" icon>
        <v-icon>mdi-close</v-icon>
      </v-btn>
      <div class="mt-5">
        <v-card-text v-for="(item, i) in item.descriptionItems" :key="i" class="pl-9 services__item">
          {{ item.item }}
        </v-card-text>
      </div>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  name: 'Dialog',
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
    iconClose: {
      type: Function,
      required: true
    }
  }
}
</script>

<style scoped>
  .services__title {
    padding-top: 30px;
    padding-bottom: 10px;
    color: #fefefe;
    font-size: 28px;
    max-width: 440px;
    margin: 0 auto;
    border-bottom: 2px solid;
  }
  .card__description {
    position: relative;
  }
  .close-icon {
    position: absolute;
    right: 0;
    top: 0;
  }
</style>
