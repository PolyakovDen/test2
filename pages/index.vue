<template>
  <div class="main__wrapper">
    <Header />
    <VideoBackground />
    <Services />
    <Cases />
  </div>
</template>

<script>
import Header from '~/components/Header'
import VideoBackground from "~/components/VideoBackground";
import Services from '~/components/Services'
import Cases from "~/components/Cases";
export default {
  components: {
    Header,
    VideoBackground,
    Services,
    Cases
  }
}
</script>

<style scoped>

</style>
