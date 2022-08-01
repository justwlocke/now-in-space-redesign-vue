<template>
  <div class="pageContainer">
    <div class="BackgroundContainer">
      <div class="container-lg">
        <!--Spacecraft-->
        <div class="row justify-content-center">
          <div class="col-3">
            <img class="spacecraft" src="./Images/SpacecraftSoyuz.png" />
          </div>
          <div class="col-2">
            <img class="spacecraft" src="./Images/SpacecraftSpaceXDragon.png" />
          </div>
        </div>
        <!-- Patches Below-->
        <div class="row justify-content-center">
          <!-- Left Crew Patch -->
          <div class="col-3 left">
            <img
              class="patchMonitor"
              src="./Images/NowInSpaceMonitorLeft.png"
            />
            <div class="patch" id="crewImage3">
              <img
                src="https://www.nasa.gov/specials/kidsclub/nowinspace/expedition67-crew4/img/slide_12.png"
              />
            </div>
          </div>

          <!-- Middle Crew Patch -->
          <div class="col-3">
            <img
              class="patchMonitor"
              src="./Images/NowInSpaceMonitorMiddle.png"
            />
            <div class="patch" id="crewImage2">
              <img
                src="https://www.nasa.gov/specials/kidsclub/nowinspace/expedition67-crew4/img/slide_12.png"
              />
            </div>
          </div>

          <!-- Right Crew Patch -->
          <div class="col-3 right">
            <img
              class="patchMonitor"
              src="./Images/NowInSpaceMonitorRight.png"
            />
            <div class="patch" id="crewImage1">
              <img
                src="https://www.nasa.gov/specials/kidsclub/nowinspace/expedition67-crew4/img/slide_12.png"
              />
            </div>
          </div>
        </div>
      </div>

      <!--Astronaut Card-->
      <div class="Astronaut" id="Cards">
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

      <!--Astronaut Carousel -->

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
          <div class="Astronaut" id="Cards">
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
        <swiper-slide>Slide 2</swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        <swiper-slide>Slide 4</swiper-slide>
        <swiper-slide>Slide 5</swiper-slide>
        <swiper-slide>Slide 6</swiper-slide>
        <swiper-slide>Slide 7</swiper-slide>
        <swiper-slide>Slide 8</swiper-slide>
        <swiper-slide>Slide 9</swiper-slide>
      </swiper>
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
