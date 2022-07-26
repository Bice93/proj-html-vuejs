<template>
  <div id="app">
    <Header/>
    <Main/>
    <Footer/>
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
    Footer,
  }
}
</script>

<style lang="scss">
@import "./styles/general.scss";
@import "./styles/variables.scss";
.container{
  width: 1500px;
  margin: 8rem auto;
}

.loop{
  font-weight: 200;
  margin: 5px 0;
  font-size: 13px;
  text-transform: uppercase;
  color: $mamba;
}

.abstract{
  font-size: 17px;
  color: $mamba;
  margin: 10px 0;
}

.btn{
  padding: 10px 20px;
  margin: 10px 0;
  border: 0px solid;
  border-radius: 7px;
  cursor: pointer;
  font-weight:700;
}

.title{
  font-size: 3rem;
  margin: 10px 0;
  color: $ColorBrand;
}
</style>
