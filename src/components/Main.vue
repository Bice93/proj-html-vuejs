<template>
  <main>
    <ProductsElement />
    <SpecialMomentElement />
  </main>
</template>

<script>
import ProductsElement from './ProductsElement.vue';
import SpecialMomentElement from './SpecialMomentsElement.vue';

export default {
    name: 'Main',
    components: {
        ProductsElement,
        SpecialMomentElement,
  }
}
</script>

<style>

</style>