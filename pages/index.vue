<template>
  <div class="main__wrapper">
    <Header />
    <VideoBackground />
    <Services />
    <Cases />
    <Advantages />
  </div>
</template>

<script>
import Header from '~/components/Header'
import VideoBackground from "~/components/VideoBackground";
import Services from '~/components/Services'
import Cases from '~/components/Cases'
import Advantages from '~/components/Advantages'
export default {
  components: {
    Header,
    VideoBackground,
    Services,
    Cases,
    Advantages
  }
}
</script>

<style scoped>

</style>
