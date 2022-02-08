<template>
  <main>
    <div class="content">
      <div class="container">
        <h2>-- Content goes here --</h2>
      </div>
    </div>
    <section id="shop">
      <div class="container">
        <div v-for="card in cards" :key="card.text" class="card-img">
          <figure>
            <img
              :src="require(`../assets/img/${card.url}`)"
              :alt="card.description"
            />
            <div>{{ card.text }}</div>
          </figure>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
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

.content {
  background-color: $c-black;
  height: 150px;
  display: flex;
  align-items: center;
}
h2 {
  color: $c-white;
}

#shop {
  position: relative;
  z-index: 1;
  color: $c-white;
  min-height: 150px;
  background-color: $c-blue;
}

.card-img figure {
  display: flex;
  align-items: center;
}
</style>
