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
          <li v-for="(link, index) in links" :key="index">
            <a :href="link.url" :class="{ active: link.active }">
              {{ link.text }}</a
            >
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      links: [
        { text: "CHARACTERS", url: "#", active: false },
        { text: "COMICS", url: "#", active: false },
        { text: "MOVIES", url: "#", active: false },
        { text: "TV", url: "#", active: false },
        { text: "GAMES", url: "#", active: false },
        { text: "COLLECTIBLES", url: "#", active: false },
        { text: "VIDEOS", url: "#", active: false },
        { text: "FANS", url: "#", active: false },
        { text: "NEWS", url: "#", active: false },
        { text: "SHOP", url: "#", active: false },
      ],
    };
  },
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
        &:hover,
        &.active {
          color: $c-blue;
        }
      }
    }
  }
}
</style>
