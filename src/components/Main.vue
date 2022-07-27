<template>
  <main>
    <ProductsElement />
    <SpecialMomentElement />
    <FreshlyBakedElement />
    <BakeryProcessElement />
  </main>
</template>

<script>
import ProductsElement from './ProductsElement.vue';
import SpecialMomentElement from './SpecialMomentsElement.vue';
import FreshlyBakedElement from './FreshlyBakedElement.vue';
import BakeryProcessElement from './BakeryProcessElement.vue';

export default {
    name: 'Main',
    components: {
        ProductsElement,
        SpecialMomentElement,
        FreshlyBakedElement,
        BakeryProcessElement,
  }
}
</script>

<style>

</style>