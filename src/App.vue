<template>
  <div>
    <Header />
    <main></main>
    <footer></footer>
  </div>
</template>

<script>
import Header from "./components/Header";
export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
