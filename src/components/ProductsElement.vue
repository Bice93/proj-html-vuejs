<template>
  <div class="container box_productsElement flex">
    <section class="element_shopping">
      <h6 class="loop">Our Products</h6>
      <h1 class="title">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit optio
        magnam veritatis.
      </h1>
      <button class="btn dark">Start Shopping</button>
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
      
      <i class="fa-solid fa-chevron-left arrow arrow_left"></i>
      <i class="fa-solid fa-chevron-right arrow arrow_right"></i>
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
          price: "19.00",
          priceKg: "39.00",
        },
        {
          img: "strawberry-jam-cookies-400x510.jpg",
          title: "Strawberry Jam Cookies",
          type: "",
          price: "24.00",
          priceKg: "62.00",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

.flex{
    justify-content: space-between;
}


.hidden{
  display: none;
}

.active{
  display: block;
}

</style>