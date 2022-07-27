<template>
  <section class="sectionCard_process">
    <div class="info_process">
      <h1>{{ elementTitle }}</h1>
      <h1>{{ id }}</h1>
      <h5> {{titleLoop}} </h5>
      <p> {{ description }} </p>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    'elementImage' : String,
    'id': String,
    'elementImg': String,
    'elementTitle': String,
    'titleLoop' : String,
    'description': String,
  },
};
</script>

<style>

</style>