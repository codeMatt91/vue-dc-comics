<template>
  <main>
    <!-- Jumbotron  -->
    <div class="jumbotron">
      <div class="container">
        <button>CURRENT SERIES</button>
      </div>
    </div>

    <!-- Section Main-Series  -->
    <div class="main-series">
      <div class="container">
        <CardImmage
          v-for="(serie, index) in series"
          :key="index"
          :serie="serie"
        />
        <div class="load"><button>LOAD MORE</button></div>
      </div>
    </div>

    <section id="shop">
      <div class="container">
        <div v-for="card in cards" :key="card.text" class="card-img">
          <figure>
            <div class="immagine">
              <img
                :src="require(`../assets/img/${card.url}`)"
                :alt="card.description"
              />
            </div>
            <div class="text">{{ card.text }}</div>
          </figure>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import CardImmage from "./CardImmage.vue";

export default {
  name: "Main",
  props: ["series"],
  components: {
    CardImmage,
  },
  data() {
    return {
      cards: [
        {
          text: "DIGITAL COMICS",
          url: "buy-comics-digital-comics.png",
          description: "logo dc",
        },
        {
          text: "DC MERCHANDISE",
          url: "buy-comics-merchandise.png",
          description: "logo merchandise",
        },
        {
          text: "SUBSCRIPTION",
          url: "buy-comics-subscriptions.png",
          description: "logo subscriptions",
        },
        {
          text: "COMIC SHOP LOCATOR",
          url: "buy-comics-shop-locator.png",
          description: "logo shop",
        },
        {
          text: "DC POWER VISA",
          url: "buy-dc-power-visa.svg",
          description: "logo visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss" served>
@import "../assets/sass/_vars.scss";
@import "../assets/sass/_generics.scss";

.main-series {
  background-color: $c-black;
  padding: 20px 0;
  .load {
    width: 100%;
    display: flex;
    justify-content: center;
    button {
      font-size: 12px;
      padding: 10px 40px;
    }
  }
}
.container {
  display: flex;
  flex-wrap: wrap;
}
.jumbotron {
  background-image: url("../assets/img/jumbotron.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  height: 400px;
  .container {
    position: relative;
    height: 100%;
    button {
      position: absolute;
      bottom: -30px;
      left: 0%;
    }
  }
}

h2 {
  color: $c-white;
}

#shop {
  position: relative;
  z-index: 1;
  color: $c-white;
  padding: 20px 0;
  background-color: $c-blue;
}

.card-img {
  width: 20%;
  figure {
    display: flex;
    align-items: center;
    .immagine {
      display: flex;
      align-items: center;
      width: 50%;
      height: 50%;
    }
    .text {
      font-size: 15px;
    }
  }
}

.card-img:last-child .immagine {
  width: 100%;
  img {
    margin-top: 15px;
  }
}
</style>
