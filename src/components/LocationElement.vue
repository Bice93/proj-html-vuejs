<template>
    <div id="location" class="container">
        <section class="title_section">
        <h6 class="loop">Locations</h6>
        <h1 class="title">Visit our Bakeries</h1>
        </section>

        <section class="cards_inline flex between">
            <CardLocation v-for="(element, index) in elementsLocation"
            :key="index"
            :image="element.img"
            :country="element.country"
            :phone="element.phoneNumber"
            :hours="element.workingHours"/>
        </section>
    </div>
</template>

<script>
import CardLocation from './CardLocation.vue';
export default {
    components:{
        CardLocation,
    },
  data: function () {
    return {
      elementsLocation: [
        {
          img: "new-york-bk-800x530.jpg",
          country: "New York",
          phoneNumber: "1.800.458.556",
          workingHours: "9:00 AM - 6:00 PM",
        },
         {
          img: "london-bk-800x530.jpg",
          country: "London",
          phoneNumber: "1.800.458.556",
          workingHours: "9:00 AM - 6:00 PM",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">

</style>