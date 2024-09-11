<script>
export default {
  data() {
    return {
      headers: [
        {
          label: "characters",
          link: "#",
          active: false,
        },
        {
          label: "comics",
          link: "#",
          active: true,
        },
        {
          label: "movie",
          link: "#",
          active: false,
        },
        {
          label: "tv",
          link: "#",
          active: false,
        },
        {
          label: "games",
          link: "#",
          active: false,
        },
        {
          label: "collectibles",
          link: "#",
          active: false,
        },
        {
          label: "videos",
          link: "#",
          active: false,
        },
        {
          label: "fans",
          link: "#",
          active: false,
        },
        {
          label: "news",
          link: "#",
          active: false,
        },
        {
          label: "shop",
          link: "#",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <div class="container-header">
        <div class="img">
          <img src="/img/dc-logo.png" alt="logo" />
        </div>
        <div class="nav-bar">
          <ul>
            <li v-for="(header, index) in headers" :key="index">
              <a
                :href="header.link"
                :class="{
                  active: header.active,
                }"
              >
                {{ header.label }}
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
@use '../assets/scss/partials/mixin' as *;
.container-header {
  @include base-flex-rule;
  align-items: center;
  width: 800px;
  margin: 0 auto;
  padding: 20px;
}
.nav-bar ul {
  list-style: none;
  display: flex;
  li {
    position: relative;
    a {
      text-decoration: none;
      color: black;
      margin-left: 5px;
      margin-right: 5px;
      font-weight: bold;
      padding: 10px 0;
      display: inline-block;
      position: relative;
      transition: color 0.3s ease;
      &::after {
        content: "";
        position: absolute;
        left: 0;
        bottom: -5px;
        height: 2px;
        background-color: blue;
        transition: width 0.3s ease;
      }
    }
  }
}
.nav-bar ul li a:hover::after,
.nav-bar ul li a.active::after {
  width: 100%;
}

.nav-bar ul li a:hover {
  color: blue;
}

.nav-bar ul li a.active {
  color: blue;
}
</style>