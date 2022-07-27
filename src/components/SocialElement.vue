<template>
  <div class="container">
    <div class="containerSocialCards">
        <CardSocial v-for="(element, index) in cardsSocial"
        :key="index"
        :image="element.img"
        :titleAlt="element.titleAlt"/>
    <!-- <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section> -->
    <!-- <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section>
    <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section>
    <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section>
    <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section>
    <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section> -->
    </div>

    <div class="socialAdded">
        <h1>Testo</h1>
    </div>
   
  </div>
</template>

<script>
import CardSocial from './CardSocial.vue';
export default {
    components:{
        CardSocial,
    },
    data: function () {
    return {
      cardsSocial: [
        {
          img: "social-1.jpg",
          titleAlt: "social-1.jpg",
        },
        {
          img: "social-2.jpg",
          titleAlt: "social-2.jpg",
        },
        {
          img: "social-3.jpg",
          titleAlt: "social-3.jpg",
        },
        {
          img: "social-4.jpg",
          titleAlt: "social-4.jpg",
        },
        {
          img: "social-5.jpg",
          titleAlt: "social-5.jpg",
        },
        {
          img: "social-6.jpg",
          titleAlt: "social-6.jpg",
        },
      ],
    };
  },
}
</script>

<style scoped lang="scss">
.container{
    position: relative;
}
.containerSocialCards{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    position: relative;
}

.socialAdded{
    width: calc(100% / 2 - 15px);
    height: 345px;
    border: 1px solid black;
    position: absolute;
    bottom: 25.2rem;
    right: 24.1rem;
}
</style>