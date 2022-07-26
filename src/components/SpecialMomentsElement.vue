<template>
  <div class="container">
    <section class="title_section">
        <h6 class="loop">Corporate &amp; Wedding</h6>
        <h1 class="title">Baking special Moments</h1>
    </section>

    <section class="cards_inline">
             <CardSpecialMoment v-for="(element, index) in specialElements" 
            :key="index"
            :SpecialElement="element.img"
            :SpecialTitle="element.title"/>
    </section>
   
  </div>
</template>

<script>
import CardSpecialMoment from "./CardSpecialMoment.vue";
export default {

components: {
    CardSpecialMoment,
  },
  data: function () {
    return {
      specialElements:[
        {
            img:"corporate-bg.jpg",
            title:"corporate.jpg",
        },
        {
            img:"wedding-bg.jpg",
            title:"wedding.jpg",
        },
      ],
    };
  },

}
</script>

<style lang="scss" scoped>
.cards_inline{
    display: flex;
    justify-content: space-between;
    margin-top: 2.5rem;
}
</style>