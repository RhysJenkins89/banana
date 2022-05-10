<template>
  <Nav />
  <Landing />
  <IntroText />
  <Products />
  <Footer />
</template>

<script>
import Nav from "./components/Nav.vue"
import Landing from "./components/Landing.vue"
import Footer from "./components/Footer.vue"
import IntroText from "./components/IntroText.vue"
import Products from "./components/Products.vue"

export default {
  name: 'App',
  components: {
    Nav,
    Landing,
    Footer,
    IntroText,
    Products
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>
