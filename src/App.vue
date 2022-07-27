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

.flex{
    display: flex;
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

.dark{
   margin-top: 2.5rem;
  background-color: $ColorBrand;
  color: $white;
    &:hover{
      background-color: $btnHover;
      color: $ColorBrand;
    }
}

.title{
  font-size: 2.5rem;
  margin: 10px 0;
  color: $ColorBrand;
}

.title_section{
    text-align: center;
}

.element_shopping {
  width: 35%;
}

.cards_inline{
    display: flex;
    justify-content: space-between;
    margin-top: 2.5rem;
}

.box_card_products {
  width: 55%;
  position: relative;
}

.arrow{
    position: relative;
    bottom: 50%;
        i{
            padding: 25px 10px;
            color: $white;
            background-color: rgba($ColorBrand, 0.4);
            cursor: pointer;
        }
}
</style>
