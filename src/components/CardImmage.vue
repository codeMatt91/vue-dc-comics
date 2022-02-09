<template>
  <div class="card-serie">
    <img :src="serie.thumb" :alt="serie.type" />
    <h5>{{ serie.series.toUpperCase() }}</h5>
  </div>
</template>

<script>
export default {
  name: "CardImmage",
  props: ["serie"],
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";

.card-serie {
  flex-basis: calc(100% / 6);
  color: $c-white;
  padding: 20px;
}
</style>
