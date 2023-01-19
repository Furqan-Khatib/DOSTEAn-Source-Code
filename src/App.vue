<template>
  <div id="app">
    <Header />
    <Carousel />
    <Tilemenudrink />
    <div
      style="
        width: 100%;
        background-color: #efefef;
        height: 6px;
        margin-top: 60px;
        border-radius: 0px;
      "
    ></div>
    <Tilemenufood />
    <div
      style="
        width: 100%;
        background-color: #efefef;
        height: 6px;
        margin-top: 60px;
        border-radius: 0px;
      "
    ></div>
    <googlemaps />
    <div>
      <footer class="footer-is-primary">
        <div class="container">
          <div class="columns">
            <div class="column">
              <p style="color: #fff">contact us</p>
            </div>
            <div class="column has-text-right">
              <a class="icon" href="#">
                facebook<i class="fa fa-facebook"></i
              ></a>
              <a class="icon" href="#">
                instagram<i class="fa fa-instagram"></i
              ></a>
            </div>
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Carousel from "./components/carousel.vue";
import Tilemenudrink from "./components/Tilemenudrink.vue";
import Tilemenufood from "./components/Tilemenufood.vue";
import googlemaps from "./components/googlemaps.vue";
import footer from "./components/footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Carousel,
    Tilemenudrink,
    Tilemenufood,
    googlemaps,
    footer,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;500&display=swap");
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Raleway", sans-serif;
  font-weight: 400;
}
.app {
  min-height: 100vh;
  position: relative;
  background-color: rgb(237, 195, 182);
}
.container {
  padding: 0 20px;
  max-width: 1140px;
  margin: 0 auto;
}

footer {
  margin-top: 40px;
  background-color: #44312b;
}

.icon {
  color: #fff;
  margin-left: 20px;
}
</style>
