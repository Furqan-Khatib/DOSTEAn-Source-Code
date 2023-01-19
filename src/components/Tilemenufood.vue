<template>
  <div class="container">
    <div class="slide-container swiper">
      <h2
        style="
          font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-weight: bold;
        "
      >
        Quick Drink
      </h2>
      <div class="slide-content">
        <div class="card-wrapper swiper-wrapper">
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/alootikki.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide2.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide3.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide4.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide5.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide6.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide7.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide8.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
          <div class="card swiper-slide">
            <div class="image-content">
              <span class="overlay"></span>

              <div class="card-image">
                <img src="../assets/slide9.jpg" alt="" class="card-img" />
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="swiper-button-next swiper-navBtn"></div>
      <div class="swiper-button-prev swiper-navBtn"></div>
      <div class="swiper-pagination"></div>
    </div>
  </div>
</template>

<script>
import { onMounted } from "vue";

export default {
  name: "Tilemenufood",
  data() {},
  mounted() {
    var swiper = new Swiper(".slide-content", {
      slidesPerView: 3,
      spaceBetween: 25,
      loop: true,
      centerSlide: "true",
      fade: "true",
      grabCursor: "true",
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
        dynamicBullets: true,
      },
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },

      breakpoints: {
        0: {
          slidesPerView: 1,
        },
        520: {
          slidesPerView: 2,
        },
        950: {
          slidesPerView: 3,
        },
      },
    });
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
.container {
  margin-top: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f4d5d5;
  border-radius: 16px;
}
.slide-container {
  max-width: 1120px;
  width: 100%;
  padding: 40px 0;
}
.slide-content {
  margin: 0 40px;
  overflow: hidden;
  border-radius: 25px;
}
.card {
  border-radius: 25px;
  background-color: #f4d5d5;
  width: 320px;
  height: 200px;
  margin: 25px;
  border-color: #f4d5d5;
}
.image-content,
.card-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-left: -20px;
  padding-right: -20px;
  padding-top: 2px;
  padding-bottom: 8px;
  width: 320px;
  height: 200px;
}
.image-content {
  row-gap: 5px;
  width: 100%;
}

.card-image {
  width: 100%;
  position: relative;
  background: #fff;
  border-radius: 25px;
}
.card-image .card-img {
  object-fit: cover;
  border-radius: 25px;
}

.button {
  border: none;
  font-size: 16px;
  color: #fff;
  padding: 8px 16px;
  background-color: #4070f4;
  border-radius: 6px;
  margin: 14px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.swiper-navBtn {
  color: #341d04;
  transition: color 0.3s ease;
}
.swiper-navBtn:hover {
  color: #432506;
}
.swiper-navBtn::before,
.swiper-navBtn::after {
  font-size: 35px;
}
.swiper-button-next {
  right: 0;
}
.swiper-button-prev {
  left: 0;
}
.swiper-pagination-bullet {
  background-color: #6e93f7;
  opacity: 1;
}
.swiper-pagination-bullet-active {
  background-color: #4070f4;
}

@media screen and (max-width: 768px) {
  .slide-content {
    margin: 0 10px;
  }
  .swiper-navBtn {
    display: none;
  }
}
</style>
