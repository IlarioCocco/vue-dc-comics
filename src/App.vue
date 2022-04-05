<template>
  <div id="app">
    <Header/>
    <main>
      <Main/>
    </main>
    <Footer :bgImage="require('./assets/img/footer-bg.jpg')"/>
  </div>
</template>





<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  }
}
</script>






<style lang="scss">
@import "./assets/scss/common.scss";
@import "./assets/scss/variables.scss";
</style>
