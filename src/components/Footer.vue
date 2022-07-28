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

        <div class="form">
          <h1 class="title">Subscribe to our Newsletter</h1>
          <input type="email" placeholder="Enter email address*">
          <button class="btn dark">Subscribe</button>
        </div>
      </section>

      <section class="row_follow_footer flex">
        <div class="box_copyright">
          	&#169; Copyright 2012 - 2020 | Avada Therme by ThermeFusion | All Rights Reserved | Powerede by WordPress
        </div>
        <div class="icon_follow">
          <ul>
            <li><a href="#"><i class="fa-brands fa-instagram"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-facebook-f"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-pinterest-p"></i></a></li>
          </ul>
        </div>
      </section>
      <section class="arrow_up">
        <a href="#anchorHeader"><i class="fa-solid fa-chevron-up"></i></a>
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
.container{
  margin-bottom: 10px;
  section{
    margin-bottom: 1.5rem;
  }
}
.box_copyright, .icon_follow, 
.box_links, .form {
  width: 50%;
}

.box_links ul{
    margin: 2rem 0;
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

.form, .icon_follow{
  text-align: end;
}

.form input{
    padding: 10px;
    width: 200px;
    margin-right: 1rem;
    height: 2.1rem;
    border-radius: 5px;
}

.box_copyright{
  color: $mamba;
}

.arrow_up{
  float: right;
  width: 50px;
  padding: 1rem;
  border-radius: 5px;
  background-color: $outerSpace;
  a{
    color: $white;
    text-decoration: none;
  }
}
</style>