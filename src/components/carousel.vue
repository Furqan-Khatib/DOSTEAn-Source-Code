<template>
  <b-container
    fluid="md"
    style="
      width: 900px;
      height: 600px;
      padding-top: 180px;
      border-radius: 10px;
      margin-bottom: 44px;
    "
  >
    <b-carousel
      controls
      indicators
      no-animation
      fade
      img-width="720"
      img-height="480"
      :interval="3000"
    >
      <b-carousel-slide caption="Welcome to Dostean" text="enjoy your meal!">
        <template v-slot:img>
          <img
            class="d-block img-fluid w-100"
            width="1080"
            height="480"
            src="../assets/slide1.jpg"
            alt="slide1"
            style="border-radius: 12px; object-fit: cover"
          />
        </template>
      </b-carousel-slide>

      <b-carousel-slide caption="Sit and Sip" text="try our out-of-the world">
        <template v-slot:img>
          <img
            class="d-block img-fluid w-100"
            width="720"
            height="480"
            src="../assets/slide2.jpg"
            alt="slide2"
            style="border-radius: 12px; object-fit: cover"
          />
        </template>
      </b-carousel-slide>

      <b-carousel-slide caption="some text" text="some more text">
        <template v-slot:img>
          <img
            class="d-block img-fluid w-100"
            width="720"
            height="480"
            src="../assets/slide3.jpg"
            alt="slide3"
            style="border-radius: 12px; object-fit: cover"
          />
        </template>
      </b-carousel-slide>
    </b-carousel>
  </b-container>
</template>

<script>
export default {
  name: "Carousel",
  props: {},
  data() {
    return {};
  },
};
</script>

<style></style>
