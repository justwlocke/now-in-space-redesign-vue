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
            el: '.custom-pagination',
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
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="First slide"
                />
                <div class="AstroImage samantha CardCrop3"></div>
                <div class="AstronautName">Bob Hines</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="third slide"
                />
                <div class="AstroImage samantha CardCrop3"></div>
                <div class="AstronautName">Oleg Artemyev</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="third slide"
                />
                <div class="AstroImage samantha CardCrop3"></div>
                <div class="AstronautName">Jessica Watkins</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <a data-bs-toggle="modal" href="#samantha-modal">
                <div class="astronaut-container">
                  <img
                    class="d-inline"
                    src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                    alt="Fourth slide"
                  />
                  <div class="AstroImage samantha CardCrop3"></div>
                  <div class="AstronautName">Samantha Cristoforetti</div>
                </div>
              </a>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="Fifth slide"
                />
                <div class="AstroImage justin CardCrop3"></div>
                <div class="AstronautName">Justin Locke</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="Sixth slide"
                />
                <div class="AstroImage docbrown CardCrop3"></div>
                <div class="AstronautName">Dr. Emmet Brown</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="Seventh slide"
                />
                <div class="AstroImage bombur CardCrop3"></div>
                <div class="AstronautName">Bombur</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="Eigth slide"
                />
                <div class="AstroImage goku CardCrop3"></div>
                <div class="AstronautName">Goku</div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="Cards">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="Ninth slide"
                />
                <div class="AstroImage missingno CardCrop3"></div>
                <div class="AstronautName">MissingNo</div>
              </div>
            </div>
          </swiper-slide>
        </swiper>

        <div class="swiper-button-next-u">
          <img src="./Images/CarouselArrowRight.png" />
        </div>

        <div
          class="custom-pagination swiper-pagination swiper-pagination-clickable swiper-pagination-bullets swiper-pagination-horizontal"
          style="bottom: -5%"
        ></div>

        <div class="swiper-button-prev-u">
          <img src="./Images/CarouselArrowLeft.png" />
        </div>

        <!--End of Carousel-->
      </div>
    </div>

    <!--Modals -->

    <div
      class="portfolio-modal modal fade"
      id="samantha-modal"
      tabindex="-1"
      role="dialog"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content astronaut-modal">
          <div class="close-modal" data-dismiss="modal">
            <div class="lr">
              <div class="rl"></div>
            </div>
          </div>
          <div class="container">
            <div class="row">
              <div class="col-lg-8 mx-auto">
                <div class="modal-body">
                  <h3>Hello</h3>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!--End Of Page Container -->
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

