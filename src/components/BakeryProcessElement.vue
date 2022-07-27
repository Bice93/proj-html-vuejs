<template>
  <div class="container box_process">
      <CardProcess
        v-for="element in elementsProcess"
        :key="element.id"
        :elementImage="element.img"
        :id="element.id"
        :elementImg="element.img"
        :elementTitle="element.title"
        :titleLoop="element.titleLoop"
        :description="element.description"
      />
      <section class="sectionCard_process">
        <h2>testo</h2>
      </section>
    
  </div>
</template>

<script>
import CardProcess from "./CardProcess.vue";
export default {
  components: {
    CardProcess,
  },

  data: function () {
    return {
      elementsProcess: [
        {
          img: "",
          title: "Tell us what you have in mind",
          id: "01",
          titleLoop: "Manual ingredients selection",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
        {
          img: "",
          title: "We Start Baking",
          id: "02",
          titleLoop: "Manual ingredients selection",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
        {
          img: "",
          title: "Delivered to your home",
          id: "03",
          titleLoop: "Manual ingredients selection",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.box_process {
  position: relative;
}

.sectionCard_process {
  height: calc(1000px / 2);
  background-color: lightblue;
  border: 1px solid black;
  margin: 10px 0;
}

.sectionCard_process:nth-child(2), .sectionCard_process:nth-child(4) {
  width: 49%;
}

.sectionCard_process:nth-child(4){
   position: absolute;
    top: 33%;
    right: 0; 
}
</style>