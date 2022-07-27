<template>
    <div class="box_elements">
        <div class="box_image">
            <img :src="require('../assets/img/'+image)" alt="">
        </div>
        <div class="info_location">
            <h1 class="title"> {{ country }} </h1>

            <ul class="infoInline">
                <li>Call us <span> {{ phone }} </span></li>
                <li>Open all Week <span> {{ hours }} </span></li>
                <li><button class="btn light">View Map</button></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        'image': String,
        'country': String,
        'phone': String,
        'hours': String,
    }
};
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

.box_elements:nth-child(1) .info_location{
  background-color: rgba($lightPurple, 0.4);
}

.box_elements {
  width: 50%;
}

.box_image img{
    width: 100%;
}

.box_image{
    line-height: 0;
}

.info_location {
    padding: 20px 0;
  text-align: center;
  background-color: rgba($chalky, 0.4);
}

.title{
    font-size: 1.8rem;
}
span {
  display: block;
}

.infoInline {
  list-style: none;
  display: flex;
  justify-content: space-around;
  align-items: center;
  li {
    line-height: 30px;
    color: $mamba;
    text-transform: uppercase;
    font-size: 14px;
  }
}
</style>