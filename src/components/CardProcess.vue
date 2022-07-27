<template>
  <section class="sectionCard_process">
    <div class="info_process">
      <div class="box_img">
        <img :src="require('../assets/img/' + elementImage)" alt="" />
      </div>
      <div class="info">
        <div class="box_title">
            <h1 class="title_process">{{ elementTitle }}</h1>
            <h1 class="id_process">{{ id }}</h1>
        </div>
        
        <div class="box_description">
            <h6 class="loop">{{ titleLoop }}</h6>
            <p>{{ description }}</p>
        </div>
       
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    elementImage: String,
    id: String,
    elementImg: String,
    elementTitle: String,
    titleLoop: String,
    description: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.loop{
  color: $white;
  font-weight: 300;
}

.sectionCard_process{
    position: relative;
}
.box_img {
  width: 100%;
  height: 100%;
    line-height: 0;
}
img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.info{
    width: 100%;
    height: 100%;
    position: absolute;
    top:0;
    left: 0;
    color: $white;
    padding: 30px;
    background-color: rgba($outerSpace, 0.6);
    .box_title{
        display: flex;
        justify-content: space-between;
    }
    .title_process{
        width: 90%;
        font-size: 3rem;
        float: left;
    }
    .id_process{
        width: 10%;
        font-size: 2rem;
        font-weight: 100;
        text-align: end;
    }
    .box_description{
        width: 30%;
        width: 30%;
        position: absolute;
        bottom: 15%;
    }
   
}

.sectionCard_process:nth-child(1) .box_description{
    right: 1%;
}

</style>