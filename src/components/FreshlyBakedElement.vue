<template>
  <div class="container box_productsElement flex">
        <section class="element_shopping">
        <h1 class="title">
            Lorem ipsum dolor sit amet consectetur.
        </h1>
        <p class="abstract">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis
            dolore error itaque quisquam nulla, pariatur sunt minus ad veritatis
            ullam eligendi quos asperiores voluptatum maiores impedit rem ducimus
            corrupti? Explicabo.
        </p>
        <button class="btn dark">Start Shopping</button>
        </section>

        <section class="box_card_products">
        <div class="ms_card flex">
            <CardFreshlyBaked
            v-for="(product, index) in freshlyProducts"
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
import CardFreshlyBaked from "./CardFreshlyBaked.vue";
export default {
  components: {
    CardFreshlyBaked,
  },

  data: function () {
    return {
      freshlyProducts: [
        {
          img: "choco-chip-cookies-200x255.jpg",
          title: "Choco Chip Cookies",
          type: "Cookies, Pastries",
          price: "19.00",
          priceKg: "39.00",
        },
        {
          img: "strawberry-jam-cookies-200x255.jpg",
          title: "Strawberry Jam Cookies",
          type: "Cookies, Pastries",
          price: "24.00",
          priceKg: "62.00",
        },
        {
          img: "strawberry-donut-200x255.jpg",
          title: "Strawberry Donut",
          type: "Cookies, Pastries",
          price: "24.00",
          priceKg: "42.00",
        },
        {
          img: "perfect-macarons-200x255.jpg",
          title: "Perfect Macarons",
          type: "Cookies, Pastries",
          price: "18.00",
          priceKg: "52.00",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

.flex {
  justify-content: space-between;
}

.element_shopping{
    text-align: center;
    align-self: center;
}

.box_card_products {
  width: 65%;
}

.element_shopping{
    width: 30%;
}
</style>