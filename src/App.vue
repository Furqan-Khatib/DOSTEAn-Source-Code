<template>
  <div id="app">
    <Header />
    <Carousel />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Carousel from "./components/carousel.vue";
import Tilemenudrink from "./components/Tilemenudrink.vue";

export default {
  name: "App",
  components: {
    Header,
    Carousel,
    Tilemenudrink,
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
</style>
