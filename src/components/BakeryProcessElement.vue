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
    <section class="sectionCard_process cardAdded">
      <div class="citation">
        <h6 class="loop">Dont just take our word for it</h6>
        <h1 class="title">
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum ea
          laudantium repellendus totam vero recusandae debitis facilis
          asperiores."
        </h1>
        <h5>Rachel Cooper, Founder</h5>
      </div>
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
          img: "bakery-process-1.jpg",
          title: "Tell us what you have in mind",
          id: "01",
          titleLoop: "Manual ingredients selection",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
        {
          img: "bakery-process-2.jpg",
          title: "We Start Baking",
          id: "02",
          titleLoop: "Manual ingredients selection",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
        {
          img: "bakery-process-3.jpg",
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

<style scoped lang="scss">
@import "../styles/variables.scss";
.box_process {
  position: relative;
}

.sectionCard_process {
  margin: 10px 0;
}

.cardAdded {
  margin: 10px 0;
  height: 575.60px;
  background-color: $pearlBush;
    .citation{
        margin: 100px auto;
        width: 70%;
            h5{
                color: $mamba;
                font-weight: 600;
            }
    }
}

.sectionCard_process:nth-child(2),
.sectionCard_process:nth-child(4) {
  width: 49%;
}

.sectionCard_process:nth-child(4) {
  position: absolute;
  top: 32.5%;
  right: 0;
}
</style>