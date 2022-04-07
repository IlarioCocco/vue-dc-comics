<template>
  <div id="app">
    <Header/>
    <main>
      <Jumbo :bgImage="require('./assets/img/jumbotron.jpg')"/>
      <Comics/>
      <Main/>
    </main>
    <Footer :bgImage="require('./assets/img/footer-bg.jpg')"/>
  </div>
</template>





<script>
import Header from './components/Header.vue';
import Jumbo from './components/Jumbo.vue';
import Comics from './components/Comics.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Jumbo,
    Comics,
    Main,
    Footer,
  }
}
</script>






<style lang="scss">
@import "./assets/scss/common.scss";
@import "./assets/scss/variables.scss";
</style>
