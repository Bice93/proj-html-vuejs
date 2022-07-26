<template>
  <div class="container box_productsElement flex">
    <section class="element_shopping">
      <h6>Our Products</h6>
      <h1>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit optio
        magnam veritatis.
      </h1>
      <button>Start Shopping</button>
    </section>

    <section class="box_card_products">
      <div class="ms_card flex">
        <CardProduct
          v-for="(product, index) in products"
          :key="index"
          :product="product.img"
          :productTitle="product.title"
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
          title: "choco-chip-cookies",
        },
        {
          img: "strawberry-jam-cookies-400x510.jpg",
          title: "strawberry-jam-cookies",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.flex{
    display: flex;
}

.element_shopping {
  width: 45%;
}

.box_card_products {
  width: 55%;
  line-height: 0;
  position: relative;
}

.ms_card {
  justify-content: space-between;
}

.arrow{
    justify-content: space-between;
    position: relative;
    bottom: 50%;
        i{
            padding: 25px 10px;
            color: $white;
            background-color: rgba($ColorBrand, 0.4);
        }
}


</style>