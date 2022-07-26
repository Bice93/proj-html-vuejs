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

    <section class="explore container">
        <h6>Fresh tasty &amp; bakery every day </h6>
        <h1>The Perfect Fresh Bread</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex et quis repellendus sit quae?</p>
        <button>Expolre our product</button>
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
  ul {
    list-style: none;
    a {
      text-decoration: none;
    }
    li {
      margin: 0 1rem;
      text-transform: uppercase;
      color: $ColorBrand;
      display: inline-block;
      padding: 7px 0;
      &:hover {
        border-bottom: 2px solid $ColorBrand;
      }
    }
  }
}
//Stile section explore
.explore{
  margin-top: 10%;
}
</style>