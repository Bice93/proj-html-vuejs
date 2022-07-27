<template>
  <main>
    <ProductsElement />
    <SpecialMomentElement />
    <FreshlyBakedElement />
  </main>
</template>

<script>
import ProductsElement from './ProductsElement.vue';
import SpecialMomentElement from './SpecialMomentsElement.vue';
import FreshlyBakedElement from './FreshlyBakedElement.vue';

export default {
    name: 'Main',
    components: {
        ProductsElement,
        SpecialMomentElement,
        FreshlyBakedElement,
  }
}
</script>

<style>

</style>