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
          <div class="patch" id="PatchLeft">
            <img
              src="https://www.nasa.gov/specials/kidsclub/nowinspace/expedition67-crew4/img/slide_12.png"
            />
          </div>
        </div>
        <div class="monitor" id="MonitorMiddle">
          <img src="./Images/NowInSpaceMonitorMiddle.png" />
          <div class="patch" id="PatchMiddle">
            <img
              src="https://www.nasa.gov/specials/kidsclub/nowinspace/expedition67-crew4/img/slide_12.png"
            />
          </div>
        </div>
        <div class="monitor" id="MonitorRight">
          <img src="./Images/NowInSpaceMonitorRight.png" />
          <div class="patch" id="PatchRight">
            <img
              src="https://www.nasa.gov/specials/kidsclub/nowinspace/expedition67-crew4/img/slide_12.png"
            />
          </div>
        </div>
      </div>

      <!--Astronaut Carousel -->

      <div class="carousel">
        <swiper
          :slidesPerView="4"
          :spaceBetween="30"
          :navigation="{
            nextEl: '.swiper-button-next-u',
            prevEl: '.swiper-button-prev-u',
          }"
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
                  src="./Images/Astronauts/CardBackgrounds/DefaultAstronautCard2.png"
                  alt="First slide"
                />
                <div class="AstroImage CardCrop"></div>
                <div class="AstronautName">Samantha Cristoforetti</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackground600x750.png"
                  alt="third slide"
                />
                <div class="AstroImage CardCrop2"></div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackground585x780G.png"
                  alt="third slide"
                />
                <div class="AstroImage CardCrop3"></div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackground580x870.png"
                  alt="Fourth slide"
                />
                <div class="AstroImage CardCrop4"></div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>Slide 5</swiper-slide>
          <swiper-slide>Slide 6</swiper-slide>
          <swiper-slide>Slide 7</swiper-slide>
          <swiper-slide>Slide 8</swiper-slide>
          <swiper-slide>Slide 9</swiper-slide>
        </swiper>

        <div class="swiper-button-next swiper-button-next-u"></div>
        <div class="swiper-button-prev swiper-button-prev-u"></div>

        <!--End of Carousel-->
      </div>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
// import required modules
import { Navigation, Pagination } from "swiper";

import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

import "./CSS/style.css";

import "./CSS/page.css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation, Pagination],
    };
  },
};
</script>

