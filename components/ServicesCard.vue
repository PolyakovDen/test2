<template>
  <div class="mb-12">
    <Dialog
      :dialog="dialog"
      :item="item"
      :handle-close="handleClose"
    />
    <div class="services__item--img-block">
      <button @click="dialog = true">
        <img class="services__item--img" :src="item.src" :alt="item.description">
      </button>
    </div>
    <p class="services__item--description">
      {{ item.description }}
    </p>
  </div>
</template>

<script>
import Dialog from '~/components/Dialog'
export default {
  name: 'ServicesCard',
  components: {
    Dialog
  },
  props: {
    item: {
      type: Object,
      required: true
    }
  },
  data: () => ({
    dialog: false
  }),
  methods: {
    handleClose () {
      this.dialog = false
    }
  }
}
</script>

<style scoped>
  .services__item--img-block {
    width: 140px;
    height: 140px;
    position: relative;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
  }

  .services__item--img {
    max-height: 100%;
    max-width: 100%;
    width: auto;
    height: auto;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    margin: auto;
  }

  .services__item--description {
    width: 120px;
    text-align: center;
    margin: 0 auto;
    font-size: 18px;
    margin-top: 15px;
  }
</style>
