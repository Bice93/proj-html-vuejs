<template>
  <header>
    <section class="header_nav">
      <!-- Logo -->
      <div class="box_logo">
        <img
          src="../assets/img/avada-bakery-logo.png"
          alt="Bakery_Logo_Brand"
        />
      </div>
      <!-- Link -->
      <div class="box_links">
        <ul>
          <li v-for="(element, index) in linksHeader" :key="index">
            <a :href="element.url"> {{ element.text }} </a>
          </li>
          <li>
            <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
          </li>
        </ul>
      </div>
    </section>

    <div class="container">
      <section class="explore">
        <h6 class="loop">Fresh tasty &amp; bakery every day </h6>
        <h1>The Perfect Fresh Bread</h1>
        <p class="abstract">Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis dolore error itaque quisquam nulla, pariatur sunt minus ad veritatis ullam eligendi quos asperiores voluptatum maiores impedit rem ducimus corrupti? Explicabo.</p>
        <button class="btn light">Explore our product</button>
      </section>
    </div>

    <section class="icon_fixed">
        <i class="fa-solid fa-clone"></i>
        <i class="fa-solid fa-tag"></i>
    </section>
    
  </header>
</template>

<script>
export default {
  name: "Header",
  data: function () {
    return {
      linksHeader: [
        {
          text: "Home",
          url: "#",
        },
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
          text: "My Account",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

header {
  background-image: url("../assets/img/hero-header-bakery.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: bottom;
  padding: 0 20px;
  height: 80vh;
}

.header_nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
// Stile Logo
.box_logo {
  width: 20%;
  img {
    width: 50%;
  }
}
// Stile link
.box_links {
  text-align: end;
  width: 80%;
  ul li{
      text-transform: uppercase;
      padding: 7px 0;
      &:hover {
        border-bottom: 2px solid $ColorBrand;
      }
  }
}
//Stile section explore
.explore{
  width: 35%;
  margin-top: 10%;
    h1{
      margin: 5px 0;
      font-size: 60px;
      color: $ColorBrand;
    }
}

.icon_fixed{
  position: fixed;
  top: 80px;
  right: 20px;
  i{
    width: 60px;
    height: 60px;
    text-align: center;
    line-height: 60px;
    background-color: $white;
    border-radius: 5px;
    display: block;
    margin: 10px 0;
    font-size: 20px;
    box-shadow: 5px 10px 18px $mamba;
  }
}

</style>