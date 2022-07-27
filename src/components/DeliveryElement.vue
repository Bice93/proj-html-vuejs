<template>
  <div class="box_delivery">
    <div class="container_small">
      <section>
        <h6 class="loop">Try our seasonal products</h6>
        <h1>Order for pick-up or delivery to your home</h1>
        <button class="btn">Shop Now</button>
      </section>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";
.box_delivery {
  background-image: url("../assets/img/call-to-action-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
.container_small {
  width: 900px;
  margin: 0 auto;
  section{
    width: 80%;
    padding: 8rem 0;
  }
  h1 {
    color: $white;
    font-size: 3rem;
    margin: 2rem 0;
  }
}

.btn {
  background-color: $white;
  color: $ColorBrand;
  &:hover {
    background-color: $ColorBrand;
    color: $white;
  }
}
</style>