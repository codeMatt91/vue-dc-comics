<template>
  <div>
    <Header />
    <Main />
    <footer></footer>
  </div>
</template>

<script>
import Header from "./components/Header";
import Main from "./components/Main";

export default {
  name: "App",
  components: {
    Header,
    Main,
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
