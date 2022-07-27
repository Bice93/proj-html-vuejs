<template>
  <div class="container box_productsElement flex">
    <section class="element_shopping">
      <h6 class="loop">Our Products</h6>
      <h1 class="title">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit optio
        magnam veritatis.
      </h1>
      <button class="btn">Start Shopping</button>
    </section>

    <section class="box_card_products">
      <div class="ms_card flex">
        <CardProduct
          v-for="(product, index) in products"
          :key="index"
          :product="product.img"
          :productTitle="product.title"
          :productType="product.type"
          :productPrice="product.price"
          :productPriceKg="product.priceKg"
        />
      </div>

      <div class="arrow flex">
        <i class="fa-solid fa-chevron-left arrow arrow_left"></i>
        <i class="fa-solid fa-chevron-right arrow_right"></i>
      </div>
    </section>
  </div>
</template>

<script>
import CardProduct from "./CardProduct.vue";
export default {
  components: {
    CardProduct,
  },
  data: function () {
    return {
      products: [
        {
          img: "choco-chip-cookies-400x510.jpg",
          title: "Choco Chip Cookies",
          type: "Cookies, Pastries",
          price: "$19.00",
          priceKg: "$39.00",
        },
        {
          img: "strawberry-jam-cookies-400x510.jpg",
          title: "Strawberry Jam Cookies",
          type: "",
          price: "",
          priceKg: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
// .box_productsElement{
//   margin-top: 8rem;
// }
.flex{
    justify-content: space-between;
}

.btn{
  margin-top: 2.5rem;
  background-color: $ColorBrand;
  color: $white;
     &:hover{
      background-color: $btnHover;
      color: $ColorBrand;
    }
}

</style>