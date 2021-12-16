<template>
  <div>
    <Header /> <!-- Qui all' interno si trovano i componenti: Contacts e Jumbotron-->

    <Main /> <!-- Qui all' interno si trovano i componenti: Presentation, MainServices, Procedure, Results, TrustedFeedback e GetInTouch -->

    <Footer /> <!-- Qui all' interno si trovano i componenti: Footer e Credits --> 
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
 
</style>
