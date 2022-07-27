<template>
  <section class="boxSocialImage">
    <img :src="require('../assets/img/'+image)" :alt="titleAlt" />
  </section>
</template>

<script>
export default {
    props:{
        'image': String,
        'titleAlt': String,
    }
};
</script>

<style scoped lang="scss">
.boxSocialImage{
    margin-bottom: 30px;
    width: calc(100% / 4 - 20px);
    line-height: 0;
        img{
            width: 100%;
        }
}

.boxSocialImage:nth-child(2), .boxSocialImage:nth-child(3){
   position: relative;
   top: 23.4rem;
}

</style>