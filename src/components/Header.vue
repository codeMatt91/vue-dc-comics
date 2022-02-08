<template>
  <header>
    <div class="container">
      <div id="logo">
        <figure>
          <a href="#"><img src="../assets/img/dc-logo.png" alt="DC logo" /></a>
        </figure>
      </div>
      <nav>
        <ul>
          <li><a href="#">CHARACTERS</a></li>
          <li><a href="#">COMICS</a></li>
          <li><a href="#"> MOVIES</a></li>
          <li><a href="#">TV</a></li>
          <li><a href="#">GAMES</a></li>
          <li><a href="#">COLLECTIBLES</a></li>
          <li><a href="#">VIDEOS</a></li>
          <li><a href="#">FANS</a></li>
          <li><a href="#">NEWS</a></li>
          <li><a href="#">SHOP</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" served>
@import "../assets/sass/_vars.scss";
@import "../assets/sass/_utils.scss";

.container {
  display: flex;
  justify-content: space-between;
}
nav {
  display: flex;

  ul {
    display: flex;
    height: $h-100;
    li {
      list-style-type: none;
      height: $h-100;
      display: flex;
      align-items: center;
      a {
        font-size: 0.8rem;
        text-decoration: none;
        color: $c-black;
        padding: 5px;
        margin: 5px;
        height: $h-100;
        display: flex;
        align-items: center;
      }
    }
  }
}
</style>
