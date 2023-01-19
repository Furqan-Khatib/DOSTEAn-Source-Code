<template>
  <header :class="{ 'scrolled-nav': scrolledNav }">
    <nav>
      <div class="branding">
        <img src="../assets/Dostean.png" alt="logo" />
        <h1 style="margin-left: 40px; padding-top: 5px">DOSTEAn</h1>
      </div>
      <ul v-show="!mobile" class="navigation">
        <li>
          <router-link class="link" :to="{ name: 'Home' }">Home</router-link>
        </li>
        <li><router-link class="link" :to="{ name: '' }">Menu</router-link></li>
        <li>
          <router-link class="link" :to="{ name: '' }">Gallery</router-link>
        </li>
        <li>
          <router-link class="link" :to="{ name: '' }">About</router-link>
        </li>
      </ul>
      <div class="icon">
        <i
          @click="toggleMobileNav"
          v-show="mobile"
          class="far fa-bars"
          :class="{ 'icon-active': mobileNav }"
        ></i>
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <li>
            <router-link class="link" :to="{ name: 'Home' }">Home</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: '' }">Menu</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: '' }">Gallery</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: '' }">About</router-link>
          </li>
        </ul>
      </transition>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {},
  data() {
    return {
      scrolledNav: null,
      mobile: null,
      mobileNav: null,
      windowWidth: null,
    };
  },

  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen();
  },
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },

  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },

    updateScroll() {
      const scrollPosition = window.scrollY;
      if (scrollPosition > 50) {
        this.scrolledNav = true;
        return;
      }
      this.scrolledNav = false;
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@font-face {
  font-family: "bastia-boldregular";
  src: url("../assets/webfontkit-20230119-095416/bastia-bold-webfont.woff2")
      format("woff2"),
    url("../assets/webfontkit-20230119-095416/bastia-bold-webfont.woff")
      format("woff");
  font-weight: normal;
  font-style: normal;
}
header {
  background-color: rgb(47, 30, 23);
  z-index: 99;
  width: 100%;
  position: fixed;
  transition: 0.5s ease all;
  color: white;
  font-family: Georgia, "Times New Roman", Times, serif;

  nav {
    position: relative;
    display: flex;
    flex-direction: row;
    padding: 12px 0;
    transition: 0.5s ease all;
    width: 90%;
    margin: 0 auto;
    @media (min-width: 1140px) {
      max-width: 1140px;
    }
    ul,
    .link {
      font-weight: 500;
      color: #fff;
      list-style: none;
      text-decoration: none;
    }

    li {
      text-transform: uppercase;
      padding: 16px;
      margin-left: 16px;
    }
    .link {
      font-size: 14px;
      transform: 0.5s ease all;
      padding-bottom: 1px solid transparent;

      &:hover {
        font-weight: bold;
        border-width: 2px;
        border-color: #fff;
      }
    }
    .branding {
      display: flex;
      align-items: center;

      img {
        width: 76px;
        transition: 0.5 ease all;
      }

      h1 {
        font-size: 46px;
        font-family: "bastia-boldregular";
        margin-bottom: 0px;
      }
    }
    .navigation {
      display: flex;
      align-items: center;
      flex: 1;
      justify-content: flex-end;
      padding-top: 20px;
    }

    .icon {
      display: flex;
      align-items: center;
      position: absolute;
      top: 0;
      right: 24px;
      height: 100%;

      i {
        cursor: pointer;
        font-size: 24px;
        transition: 0.8s ease all;
      }
    }

    .icon-active {
      transform: rotate(180deg);
    }

    .dropdown-nav {
      display: flex;
      flex-direction: column;
      position: fixed;
      width: 100%;
      max-width: 250px;
      height: 100%;
      background-color: #fff;
      top: 0;
      left: 0;

      li {
        margin-left: 0;
        .link {
          color: #000;
        }
      }
    }

    .mobile-nav-enter-active,
    .mobile-nav-leave-active {
      transition: 1s ease all;
    }

    .mobile-nav-enter-from,
    .mobile-nav-leave-to {
      transform: translateX(-250px);
    }

    .mobile-nav-enter-to {
      transform: translateX(0);
    }
  }
}

.scrolled-nav {
  background-color: rgb(44, 30, 25);
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);

  nav {
    padding: 0px 0;

    .branding {
      img {
        width: 62px;
        transition: 0.5s;
        box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
          0 2px 4px -1px rgba(0, 0, 0, 0.06);
      }

      h1 {
        font-size: 42px;
        transition: 0.5s;
      }
    }
  }
}
</style>
