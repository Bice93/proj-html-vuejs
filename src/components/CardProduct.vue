<template>
    <div class="card">
      <img :src="require('../assets/img/' + product)" :alt="productTitle" />
      <span class="info_card">
        <h1>{{ viewElement(productTitle) }}</h1>
        <h4>{{ viewElement(productType) }}</h4>
        <h2>$ {{ viewElement(productPrice) }} - $ {{ viewElement(productPriceKg) }}</h2>
      </span>
    </div>
</template>

<script>
export default {
  props: {
    product: String,
    productTitle: String,
    productType: String,
    productPrice: String,
    productPriceKg: String,
  },

  methods:{
    viewElement(element){
      if(element != "" || null){
        return element;
      };
    },
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.card {
  cursor: pointer;
  position: relative;
  &:hover .info_card {
    display: block;
  }
  img{
    height: 100%;
    width: 100%;
  }
}
.info_card {
  width: 100%;
  height: 100%;
  padding-top: 12rem;
  display: none;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgba($outerSpace, 0.3);
  color: $white;
  text-align: center;
  * {
    margin: 9px 0;
  }
  h4 {
    font-weight: 100;
  }
}
</style>