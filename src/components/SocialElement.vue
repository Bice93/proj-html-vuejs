<template>
  <div id="socialGallery" class="container">
    <div class="containerSocialCards flex between">
        <CardSocial v-for="(element, index) in cardsSocial"
        :key="index"
        :image="element.img"
        :titleAlt="element.titleAlt"/>
    </div>

    <div class="socialAdded">
        <div>
            <h6 class="loop">Made for sharing</h6>
            <h1 class="title">Let's stay in touch</h1>
            <button class="btn dark"><i class="fa-brands fa-instagram"></i> Follow us</button>
        </div>
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
@import "../styles/variables.scss";
.container{
    position: relative;
}
.containerSocialCards{
    flex-wrap: wrap;
    position: relative;
}

.socialAdded{
    width: calc(100% / 2 - 15px);
    height: 345px;
    background-color: rgba($lightPurple, 0.1);
    position: absolute;
    bottom: 25.3rem;
    right: 24.1rem;
    text-align: center;
    div{
        margin-top: 5rem;

        i{
            margin-right: 10px;
        }
    }
}
</style>