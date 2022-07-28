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
//Stile contenitore
.container{
  width: 1500px;
  margin: 8rem auto;
}
//classe flex
.flex{
    display: flex;
}

.between{
  justify-content: space-between;
}

//stile dei titoli
.loop{
  font-weight: 600;
  margin: 10px 0;
  font-size: 13px;
  text-transform: uppercase;
  color: $mamba;
}

.title{
  font-size: 2.5rem;
  margin: 10px 0;
  color: $ColorBrand;
}

.abstract{
  font-size: 17px;
  color: $mamba;
  margin: 10px 0;
}
//Stile lista
ul{
  list-style: none;
    li{
       color: $ColorBrand;
      display: inline-block;
      margin: 0 1rem;
    }
    a{
      text-decoration: none;
    }
}
//Stile bottoni
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

.light{
  background-color: $white;
  color: $ColorBrand;
    &:hover{
      background-color: $ColorBrand;
      color: $white;
    }
}

.title_section{
    text-align: center;
}

.element_shopping {
  width: 35%;
  align-self: center;
}

.cards_inline{
    margin-top: 2.5rem;
}

.box_card_products {
  width: 55%;
  position: relative;
}

//Stile frecce di next e previous
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
