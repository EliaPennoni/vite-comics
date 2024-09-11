<script>
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
      apps: [
        {
          img: "/img/footer-facebook.png",
        },
        {
          img: "/img/footer-periscope.png",
        },
        {
          img: "/img/footer-pinterest.png",
        },
        {
          img: "/img/footer-twitter.png",
        },
        {
          img: "/img/footer-youtube.png",
        },
      ],
    };
  },
};
</script>

<template>
  <main>
    <div class="content-container">
      <h2>--&gt; content goes here &lt;--</h2>
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
.content-container {
  background-color: black;
  height: 150px;
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
    height: 100%;
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