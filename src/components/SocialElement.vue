<template>
  <div class="container">
    <div class="containerSocialCards">
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
    </section>
    <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section>
    <section class="boxSocialImage">
        <img src="../assets/img/social-1.jpg" alt="">
    </section>
    </div>

    <div class="socialAdded">
        <h1>Testo</h1>
    </div>
   
  </div>
</template>

<script>
export default {

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

.socialAdded{
    width: calc(100% / 2 - 15px);
    height: 345px;
    border: 1px solid black;
    position: absolute;
    bottom: 25.2rem;
    right: 24.1rem;
}
</style>