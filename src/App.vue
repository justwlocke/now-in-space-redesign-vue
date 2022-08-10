<template>
  <div class="pageContainer">
    <img class="backgroundImage" src="./Images/NowInSpaceBackground2.png" />
    <div class="ContentsContainer">
      <div class="spaceships">
        <img id="Ship1" src="./Images/SpacecraftSpaceXDragon.png" />
        <img id="Ship2" src="./Images/SpacecraftSoyuz.png" />
      </div>

      <div class="expeditionMonitors">
        <div class="monitor" id="MonitorLeft">
          <img src="./Images/NowInSpaceMonitorLeft.png" />
        </div>
        <div class="monitor" id="MonitorMiddle">
          <!--<img src="./Images/NowInSpaceMonitorMiddle.png" />-->
        </div>
        <div class="monitor" id="MonitorRight"></div>
      </div>

      <!--Astronaut Carousel -->

      <div class="carousel">
        <swiper
          :slidesPerView="4"
          :spaceBetween="30"
          :pagination="{
            clickable: true,
          }"
          :modules="modules"
          class="mySwiper"
        >
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/DefaultAstronautCard2.png"
                  alt="First slide"
                />
                <div class="AstroImage CardCrop"></div>
                <div class="AstronautName">Samantha Cristoforetti</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>Slide 2 But then some extra text happens</swiper-slide>
          <swiper-slide>Slide 3</swiper-slide>
          <swiper-slide>Slide 4</swiper-slide>
          <swiper-slide>Slide 5</swiper-slide>
          <swiper-slide>Slide 6</swiper-slide>
          <swiper-slide>Slide 7</swiper-slide>
          <swiper-slide>Slide 8</swiper-slide>
          <swiper-slide>Slide 9</swiper-slide>
        </swiper>
      </div>

      <!--End of Carousel-->
    </div>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

import "./CSS/style.css";

import "./CSS/page.css";

// import required modules
import { Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>
