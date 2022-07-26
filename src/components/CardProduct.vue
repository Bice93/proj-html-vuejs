<template>
  <div>
    <img :src="require('../assets/img/'+product)" :alt="productTitle">
  </div>
</template>

<script>
export default {
    props:{
        'product': String,
        'productTitle': String,
    }
}
</script>

<style lang="scss" scoped>

</style>