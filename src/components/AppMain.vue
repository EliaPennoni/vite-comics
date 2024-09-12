<script>
import SingleCard from "./SingleCard.vue";
export default {
  data() {
    return {
      cards: [
        {
          img: "/img/buy-comics-digital-comics.png",
          link: "digital comics",
          active: false,
        },
        {
          img: "/img/buy-comics-merchandise.png",
          link: "dc merchandise",
          active: false,
        },
        {
          img: "/img/buy-dc-power-visa.svg",
          link: "subscriptions",
          active: false,
        },
        {
          img: "/img/buy-comics-subscriptions.png",
          link: "digital comics",
          active: false,
        },
        {
          img: "/img/buy-comics-shop-locator.png",
          link: "digital comics",
          active: false,
        },
      ],
      dccomics: [
        {
          label: "Characters",
          link: "#",
          active: "false",
        },
        {
          label: "Comics",
          link: "#",
          active: "false",
        },
        {
          label: "moviess",
          link: "#",
          active: "false",
        },
        {
          label: "Tv",
          link: "#",
          active: "false",
        },
        {
          label: "Games",
          link: "#",
          active: "false",
        },
        {
          label: "News",
          link: "#",
          active: "false",
        },
      ],
      dcs: [
        {
          label: "Term of use",
          link: "#",
          active: "false",
        },
        {
          label: "Privacy policy",
          link: "#",
          active: "false",
        },
        {
          label: "Add choices",
          link: "#",
          active: "false",
        },
        {
          label: "Advertising",
          link: "#",
          active: "false",
        },
        {
          label: "Jobs",
          link: "#",
          active: "false",
        },
        {
          label: "Subscriptions",
          link: "#",
          active: "false",
        },
        {
          label: "Talents",
          link: "#",
          active: "false",
        },
        {
          label: "Ratings",
          link: "#",
          active: "false",
        },
        {
          label: "Shop",
          link: "#",
          active: "false",
        },
        {
          label: "Contact us",
          link: "#",
          active: "false",
        },
        {
          label: "News",
          link: "#",
          active: "false",
        },
      ],
      shops: [
        {
          label: "Shop DC",
          link: "#",
          active: "false",
        },
        {
          label: "Contact Us",
          link: "#",
          active: "false",
        },
      ],
      sites: [
        {
          label: "Talents",
          link: "#",
          active: "false",
        },
        {
          label: "Ratings",
          link: "#",
          active: "false",
        },
        {
          label: "Shop",
          link: "#",
          active: "false",
        },
        {
          label: "Contact us",
          link: "#",
          active: "false",
        },
        {
          label: "News",
          link: "#",
          active: "false",
        },
      ],
    

      fumetti: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
  components: {
    SingleCard,
  },
};
</script>

<template>
  <main>
    <div class="jumbotron"></div>
    <div class="content-container">
      <div class="comics-container">
        <SingleCard
          class="comics"
          v-for="(fumetto, index) in fumetti"
          :key="index"
          :product="fumetto"
        />
        <!-- <img :src="fumetto.thumb" alt="" />
          <h6>{{ fumetto.series }}</h6> -->
      </div>
    </div>
    <div class="card-background">
      <div class="card-container">
        <div class="card" v-for="(card, index) in cards" :key="index">
          <img :src="card.img" alt="" />
          <h6>
            {{ card.link }}
          </h6>
        </div>
      </div>
    </div>
    <div class="background-column-container">
      <div class="column-container">
        <div class="left-col">
          <div class="dc-comics">
            <h4>Dc Comics</h4>
            <ul>
              <li v-for="(comic, index) in dccomics" :key="index">
                <a href="#">{{ comic.label }}</a>
              </li>
            </ul>
            <div class="shop">
              <h4>Shop</h4>
              <ul>
                <li v-for="(shop, index) in shops" :key="index">
                  <a href="#">{{ shop.label }}</a>
                </li>
              </ul>
            </div>
          </div>
          <div class="dc">
            <h4>DC</h4>
            <ul>
              <li v-for="(dc, index) in dcs" :key="index">
                <a href="#">{{ dc.label }}</a>
              </li>
            </ul>
          </div>
          <div class="sites">
            <h4>Sites</h4>
            <ul>
              <li v-for="(site, index) in sites" :key="index">
                <a href="#">{{ site.label }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="right-col">
          <img src="/img/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/mixin.scss" as *;

.comics-container {
  background-color: black;
  display: flex;
  flex-wrap: wrap;
  width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.jumbotron {
  background-image: url(/public/img/jumbotron.jpg);
  height: 400px;
}
.content-container {
  background-color: black;
  h2 {
    color: white;
    text-align: center;
  }
}

.card-background {
  background-color: blue;
  height: 150px;
  display: flex;
  z-index: 999;
}
.card-container {
  margin: 0 auto;
  width: 800px;
  display: flex;
  align-items: center;
  padding: 20px;
}

.card {
  display: flex;
  align-items: center;
  width: 20%;
  margin-right: 10px;
  h6 {
    color: white;
    margin-left: 15px;
  }
  img {
    width: 30%;
    height: 1;
  }
}

.background-column-container {
  background-image: url(/img/footer-bg.jpg);
}

.column-container {
  display: flex;
  align-items: center;
  width: 800px;
  margin: 0 auto;
}

.left-col {
  display: flex;
  padding: 20px;
}
.dc-comics {
  display: flex;
  flex-direction: column;
  color: white;
  margin-right: 30px;
}
.dc-comics ul {
  @include base-decoration-rule;
  li a {
    list-style: none;
    text-decoration: none;
    color: darkgray;
    font-size: small;
    &:hover {
      color: white;
    }
  }
}

.shop {
  display: flex;
  flex-direction: column;
  margin-top: 15px;
  ul {
    @include base-decoration-rule;
    li a {
      @include base-decoration-rule;
      color: darkgray;
      font-size: small;
    }
  }
}

.dc {
  display: flex;
  flex-direction: column;
  color: white;
  margin-right: 30px;
  ul {
    @include base-decoration-rule;
    li a {
      @include base-decoration-rule;
      color: darkgray;
      font-size: small;
      &:hover {
        color: white;
      }
    }
  }
}

.sites {
  display: flex;
  flex-direction: column;
  color: white;
  ul {
    @include base-decoration-rule;
    li a {
      list-style: none;
      text-decoration: none;
      color: darkgray;
      font-size: small;
      &:hover {
        color: white;
      }
    }
  }
}

.right-col {
  position: relative;
  width: 50%;
  height: 300px;
  overflow: hidden;
  z-index: 1;
  img {
    position: absolute;
    top: 0;
    width: 100%;
    height: auto;
    z-index: -1;
  }
}
</style>