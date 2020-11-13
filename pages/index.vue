<template>
  <div class="main__wrapper">
    <Header />
    <Services />
    <Cases />
  </div>
</template>

<script>
import Header from '~/components/Header'
import Services from '~/components/Services'
import Cases from "~/components/Cases";
export default {
  components: {
    Header,
    Services,
    Cases
  }
}
</script>

<style scoped>

</style>
