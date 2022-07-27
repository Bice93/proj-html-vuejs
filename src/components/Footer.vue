<template>
  <footer>
    <div class="container">
      <section class="row_nav_footer flex">
        <div class="box_links">
          <img
            src="../assets/img/avada-bakery-logo.png"
            alt="avada-bakery-logo.png"
          />
          <ul>
            <li v-for="(element, index) in linksFooter" :key="index">
              <a :href="element.url"> {{ element.text }} </a>
            </li>
            <li>
              <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
              <section class="numbers_order"> 0 </section>
            </li>
          </ul>
        </div>

        <div class="form"></div>
      </section>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",

  data: function () {
    return {
      linksFooter: [
        {
          text: "Shop",
          url: "#",
        },
        {
          text: "About",
          url: "#",
        },
        {
          text: "Gallery",
          url: "#",
        },
        {
          text: "Location",
          url: "#",
        },
        {
          text: "Journal",
          url: "#",
        },
        {
          text: "Contact",
          url: "#",
        },
        {
          text: "Orders",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.box_links{
  width: 50%;
    ul{
      margin: 2rem 0;
    }
    .numbers_order{
      display: inline-block;
      width: 30px;
      height: 30px;
      background-color: rgba($lightPurple, 0.1);
      margin-left: .4rem;
      text-align: center;
      line-height: 30px;
      border-radius: 50%;
      font-size: 1.2rem;
    }
}
.form {
  width: 50%;
}
</style>