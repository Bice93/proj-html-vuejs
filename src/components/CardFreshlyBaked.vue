<template>
  <div class="card_freshly">
    <div class="box_imgFreshly">
      <img :src="require('../assets/img/' + product)" :alt="productTitle" />
      <span>
        <h1>Select Options / Quick View</h1>
      </span>
    </div>

    <div class="info_card_freshly">
      <h1>{{ productTitle }}</h1>
      <h2>${{ productPrice }} - ${{ productPriceKg }}</h2>
    </div>
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

.card_freshly {
  width: 24%;
  cursor: pointer;
    img {
        width: 100%;
    }
    &:hover span {
        display: block;
    }
}

.box_imgFreshly {
  width: 100%;
  line-height: 0;
  position: relative;
    span {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        height: 100%;
        background-color: rgba($mamba, 0.3);
        text-align: center;
        display: none;
        h1 {
        font-size: 16px;
        line-height: 300px;
        color: $white;
        text-transform: uppercase;
        }
    }
}

.info_card_freshly {
  padding: 5px 0;
  width: 100%;
  color: $ColorBrand;
  font-size: 14px;
  text-align: center;
    * {
        margin: 5px 0;
    }
    h2 {
        font-weight: 100;
        font-size: 1rem;
    }
}
</style>