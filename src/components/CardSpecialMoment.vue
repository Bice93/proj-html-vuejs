<template>
  <div class="card_special">
    <img
      :src="require('../assets/img/' + SpecialElement)"
      :alt="SpecialTitle"
    />
    <div class="card_special_hover">
      <img
        :src="require('../assets/img/' + SpecialElementHover)"
        :alt="titleAlt"
      />
      <span class="info_card_special">
        <h6>{{ titleLoop }}</h6>
        <h1>{{ titleHover }}</h1>
        <button class="btn dark">{{ btn }}</button>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    SpecialElement: String,
    SpecialTitle: String,
    SpecialElementHover: String,
    titleAlt: String,
    titleLoop: String,
    titleHover: String,
    btn: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.card_special {
  position: relative;
  width: 48%;
  img {
    width: 100%;
    object-fit: cover;
  }
  &:hover .card_special_hover{
    display: block;
  }
}

.card_special_hover {
  position: relative;
  position: absolute;
  top: 0;
  display: none;
}

.info_card_special {
  width: 80%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: $white;
  text-align: center;
  * {
    margin: 9px 0;
  }
  h6 {
    text-transform: uppercase;
    font-weight: 100;
  }
  h1 {
    font-size: 2rem;
  }
}
</style>