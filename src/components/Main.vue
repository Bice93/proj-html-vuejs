<template>
  <main>
    <ProductsElement />
    <SpecialMomentElement />
    <FreshlyBakedElement />
    <BakeryProcessElement />
    <LocationElement />
  </main>
</template>

<script>
import ProductsElement from './ProductsElement.vue';
import SpecialMomentElement from './SpecialMomentsElement.vue';
import FreshlyBakedElement from './FreshlyBakedElement.vue';
import BakeryProcessElement from './BakeryProcessElement.vue';
import LocationElement from './LocationElement.vue';

export default {
    name: 'Main',
    components: {
        ProductsElement,
        SpecialMomentElement,
        FreshlyBakedElement,
        BakeryProcessElement,
        LocationElement,
  }
}
</script>

<style>

</style>