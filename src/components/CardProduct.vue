<template>
    <div class="card">
      <img :src="require('../assets/img/' + product)" :alt="productTitle" />
      <span
        v-if="productTitle && productType && productPrice && productPriceKg"
        class="info_card"
      >
        <h1>{{ productTitle }}</h1>
        <h4>{{ productType }}</h4>
        <h2>{{ productPrice }} - {{ productPriceKg }}</h2>
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
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.card {
  position: relative;
  &:hover .info_card {
    display: block;
  }
}
.info_card {
  width: 80%;
  display: none;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
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