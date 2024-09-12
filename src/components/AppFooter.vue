<script>
export default {
  data() {
    return {
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
  <footer>
    <div class="footer-background">
      <div class="left-foot">
        <button>SIGN-UP NOW</button>
      </div>
      <div class="foot-icons">
        <h4>FOLLOW US ON</h4>
        <ul>
          <li v-for="(app, index) in apps" :key="index">
            <a href="#">
              <img :src="app.img" alt="" />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/mixin.scss" as *;

.card-background,
footer {
  position: relative;
  z-index: 10;
}
.dc-comics ul,
.shop ul,
.dc ul,
.sites ul {
  padding: 0;
  margin: 0;
}
footer {
  background-color: rgb(54, 53, 53);
  z-index: 999;
}
.footer-background {
  display: flex;
  align-items: center;
  width: 800px;
  margin: 0 auto;
  padding: 20px;
  justify-content: space-between;
}
.foot-icons {
  display: flex;
  align-items: center;
  ul {
    display: flex;
    align-items: center;
    list-style: none;
    text-decoration: none;
    li a {
      margin-right: 15px;
    }
  }
  h4 {
    color: blue;
  }
}
button {
  border: 3px solid blue;
  padding: 10px;
  color: white;
  background-color: rgb(54, 53, 53);
  cursor: pointer;
}
</style>