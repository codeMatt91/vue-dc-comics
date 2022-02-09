<template>
  <main>
    <!-- Jumbotron  -->
    <div class="jumbotron"></div>

    <!-- Section Main-Series  -->
    <div class="main-series">
      <div class="container">
        <div v-for="(serie, index) in series" :key="index" class="card-serie">
          <img :src="serie.thumb" :alt="serie.type" />
          <h5>{{ serie.series.toUpperCase() }}</h5>
        </div>
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
      series: [
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
};
</script>

<style lang="scss" served>
@import "../assets/sass/_vars.scss";

.main-series {
  background-color: $c-black;
  padding: 30px 0;
}
.container {
  display: flex;
  flex-wrap: wrap;
}
.card-serie {
  flex-basis: calc(100% / 6);
  color: $c-white;
  padding-bottom: 20px;
  .img {
    height: 50%;
  }
}
.jumbotron {
  background-image: url("../assets/img/jumbotron.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  min-height: 300px;
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
