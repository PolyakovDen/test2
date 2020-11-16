<template>
  <div class="main__wrapper">
    <Header />
    <VideoBackground />
    <Services />
    <Cases />
    <Advantages />
    <Form />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header'
import VideoBackground from '~/components/VideoBackground'
import Services from '~/components/Services'
import Cases from '~/components/Cases'
import Advantages from '~/components/Advantages'
import Form from '~/components/Form'
import Footer from '~/components/Footer'
export default {
  components: {
    Header,
    VideoBackground,
    Services,
    Cases,
    Advantages,
    Form,
    Footer
  }
}
</script>

<style scoped>

</style>
