<template>
  <div class="">
    <Header />
    <Privacy />
    <Footer />
  </div>
</template>

<script>
  import Header from "~/components/Header";
  import Privacy from "~/components/Privacy";
  import Footer from "~/components/Footer";
  export default {
    components: {
      Header,
      Privacy,
      Footer
    }
  }
</script>
