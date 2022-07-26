<template>
  <div class="card_special">
    <img :src="require('../assets/img/' + SpecialElement)" :alt="SpecialTitle">
  </div>
</template>

<script>
export default {
    props: {
    'SpecialElement': String,
    'SpecialTitle': String,
  },
}
</script>

<style lang="scss" scoped>
.card_special{
    width: 48%;
        img{
            width: 100%;
            object-fit: cover;
        }
}
</style>