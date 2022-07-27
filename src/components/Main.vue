<template>
  <main>
    <ProductsElement />
    <SpecialMomentElement />
    <FreshlyBakedElement />
    <BakeryProcessElement />
    <LocationElement />
    <SocialElement />
  </main>
</template>

<script>
import ProductsElement from './ProductsElement.vue';
import SpecialMomentElement from './SpecialMomentsElement.vue';
import FreshlyBakedElement from './FreshlyBakedElement.vue';
import BakeryProcessElement from './BakeryProcessElement.vue';
import LocationElement from './LocationElement.vue';
import SocialElement from './SocialElement.vue';

export default {
    name: 'Main',
    components: {
        ProductsElement,
        SpecialMomentElement,
        FreshlyBakedElement,
        BakeryProcessElement,
        LocationElement,
        SocialElement,
  }
}
</script>

<style>

</style>