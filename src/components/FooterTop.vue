<template>
  <div class="footer-top">
    <div class="container">
      <div id="links">
        <div v-for="(link, index) in links" :key="index">
          <h3>{{ link.title }}</h3>
          <ul>
            <li v-for="(item, index) in link.array" :key="index">{{ item }}</li>
          </ul>
        </div>
      </div>
      <div class="logo">
        <figure>
          <img src="../assets/img/dc-logo-bg.png" alt="Logo dc" />
        </figure>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterTop",
  data() {
    return {
      links: [
        {
          title: "DC COMICS",
          array: [
            "Characters",
            "Comics",
            "Movies",
            "Tv",
            "Games",
            "Video",
            "News",
          ],
        },
        {
          title: "SHOP",
          array: ["Shop DC", "Shop DC Collectible"],
        },
        {
          title: "DC",
          array: [
            "Term of use",
            "Privacy policy",
            "Add Choise",
            "Advertising",
            "Jobs",
            "Subscription",
            "Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          array: ["DC", "MAD Megazine", "DC Universe", "DC Power Visa"],
        },
      ],
    };
  },
};
</script>

<style lang="scss" served>
@import "../assets/sass/_vars.scss";

.footer-top {
  position: relative;
  display: flex;
  align-items: center;
  height: 600px;
  color: $c-white;
  background-image: url("../assets/img/footer-bg.jpg");
  max-height: 350px;
}

#links {
  width: 50%;
  display: flex;
  flex-wrap: wrap;
  h3 {
    padding: 0 0 10px 10px;
  }
  ul {
    margin: 0 10px;
    list-style-type: none;
    align-content: space-around;
    li {
      color: grey;
    }
  }
}

.logo {
  position: absolute;
  right: 116px;
  bottom: -75px;
  z-index: 0;
  img{
     width: 90%;
  }
}
</style>
