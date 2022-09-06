<template>
  <div class="pageContainer">
    <img class="backgroundImage" src="./Images/NowInSpaceBackground2.png" />
    <div class="ContentsContainer">
      <div class="spaceships">
        <a data-bs-toggle="modal" href="#spaceX-modal">
          <img id="Ship1" src="./Images/SpacecraftSpaceXDragon.png" />
        </a>
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
        <main id="swiper-contain">
          <swiper
            :modules="modules"
            :slides-per-view="4"
            :slides-per-group="4"
            :loopedSlides="8"
            :loop="false"
            :centeredSlides="false"
            :space-between="25"
            :speed="500"
            :preloadImages="false"
            :lazy="{
              loadPrevNext: true,
              loadOnTransitionStart: true,
              loadPrevNextAmount: 2,
            }"
            :navigation="true"
            :pagination="{
              clickable: true,
            }"
            :watchSlidesProgress="true"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
          >
            <swiper-slide>
              <div class="Cards">
                <div class="astronaut-container">
                  <img
                    class="d-inline"
                    src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                    alt="First slide"
                  />
                  <div class="AstroImage bob CardCrop3"></div>
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
                  <div class="AstroImage oleg CardCrop3"></div>
                  <div class="AstronautName">Oleg Artemyev</div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="Cards">
                <a data-bs-toggle="modal" href="#jessica-modal">
                  <div class="astronaut-container">
                    <img
                      class="d-inline"
                      src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                      alt="third slide"
                    />
                    <div class="AstroImage jessica CardCrop3"></div>
                    <div class="AstronautName">Jessica Watkins</div>
                  </div>
                </a>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="Cards">
                <a data-bs-toggle="modal" href="#samantha-modal">
                  <div class="astronaut-container card-shadow">
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
            ...
          </swiper>
        </main>
      </div>
      <!--End of Carousel-->
    </div>
    <!--End of Contents Container-->

    <!--Modals -->
    <div
      class="portfolio-modal modal fade"
      id="spaceX-modal"
      tabindex="-1"
      role="dialog"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content ship-modal">
          <div class="modal-header">
            <img
              class="modal-ship-img"
              src="./Images/SpacecraftSpaceXDragon.png"
            />
            <span class="modal-ship-name"> Space X Dragon </span>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <div class="modal-ship-details">
              <p>
                SpaceX something something in space. Going to type a lot of text
                here to see what it looks like. Hmm. Texty-text-text. Lorum
                Ipsum. Bacon. Lightfall.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div
      class="portfolio-modal modal fade"
      id="jessica-modal"
      tabindex="-1"
      role="dialog"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content astronaut-modal">
          <div class="modal-header">
            <div class="Cards modal-card">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="Jessica Watkins"
                />
                <div class="AstroImage jessica CardCrop3"></div>
                <div class="AstronautName modal-astro-card-name">
                  Jessica Watkins
                </div>
              </div>
            </div>
            <span class="modal-astro-name"> Jessica Watkins </span>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <div class="modal-astro-details">
              <p>
                Jessica something something in space. Going to type a lot of
                text here to see what it looks like. Hmm. Texty-text-text. Lorum
                Ipsum. Bacon. Lightfall.
              </p>
            </div>
          </div>
          <div class="modal-footer">
            <a data-bs-toggle="modal" href="#-modal">
              <div class="modal-prev-astro">
                <img src="./Images/CarouselArrowLeft.png" />
                <p class="modal-astro-arrows-prev">PREVIOUS ASTRONAUT</p>
              </div>
            </a>
            <a data-bs-toggle="modal" href="#samantha-modal">
              <div class="modal-next-astro">
                <img src="./Images/CarouselArrowRight.png" />
                <p class="modal-astro-arrows-next">NEXT ASTRONAUT</p>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>

    <div
      class="portfolio-modal modal fade"
      id="samantha-modal"
      tabindex="-1"
      role="dialog"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content astronaut-modal">
          <div class="modal-header">
            <div class="Cards modal-card">
              <div class="astronaut-container">
                <img
                  class="d-inline"
                  src="./Images/Astronauts/CardBackgrounds/CardBackgroundBlue585x780.png"
                  alt="Samantha Cristoforetti"
                />
                <div class="AstroImage samantha CardCrop3"></div>
                <div class="AstronautName modal-astro-card-name">
                  Samantha Cristoforetti
                </div>
              </div>
            </div>
            <span class="modal-astro-name"> Samantha Cristoforetti </span>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <div class="modal-astro-details">
              <p>
                Samantha something something in space. Going to type a lot of
                text here to see what it looks like. Hmm. Texty-text-text. Lorum
                Ipsum. Bacon. Lightfall.
              </p>
            </div>
          </div>
          <div class="modal-footer">
            <a data-bs-toggle="modal" href="#jessica-modal">
              <div class="modal-prev-astro">
                <img src="./Images/CarouselArrowLeft.png" />
                <p class="modal-astro-arrows-prev">PREVIOUS ASTRONAUT</p>
              </div>
            </a>
            <a data-bs-toggle="modal" href="#-modal">
              <div class="modal-next-astro">
                <img src="./Images/CarouselArrowRight.png" />
                <p class="modal-astro-arrows-next">NEXT ASTRONAUT</p>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>

    <!--End Of Page Container -->
  </div>
</template>

<script>
// import Swiper core and required modules
import { Navigation, Pagination } from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

import "./CSS/style.css";

import "./CSS/page.css";

export default {
  name: "astro-carousel",
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




