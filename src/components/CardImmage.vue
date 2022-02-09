<template>
  <div class="card-serie">
    <img :src="thumb" :alt="type" />
    <h5>{{ series.toUpperCase() }}</h5>
  </div>
</template>

<script>
export default {
  name: "CardImmage",
  props: ["thumb", "series", "type"],
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";

.card-serie {
  flex-basis: calc(100% / 6);
  color: $c-white;
  padding-bottom: 20px;
  .img {
    height: 50%;
  }
}
</style>
