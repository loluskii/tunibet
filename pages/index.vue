<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333; z-index: -1"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide img-src="~/assets/img/wop.png"></b-carousel-slide>

      <b-carousel-slide img-src="~/assets/img/wop-2.png"> </b-carousel-slide>

      <b-carousel-slide img-src="~/assets/img/wop-3.png"> </b-carousel-slide>
    </b-carousel>

    <div class="container-fluid px-4 body-section">
      <div class="row mb-4">
        <div class="col-6 col-lg-2 mb-2 pr-sm-2 pr-0">
          <nuxt-link to="">
            <div class="card landing-card">
              <div class="card-body d-flex align-items-center flex-column">
                <img src="~/assets/img/Sport.png" />
                <p class="mb-0 mt-auto">SPORT</p>
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="col-6 col-lg-2 mb-2">
          <nuxt-link to="">
            <div class="card landing-card">
              <div class="card-body d-flex align-items-center flex-column">
                <img src="~/assets/img/live.png" />
                <p class="mb-0 mt-auto">LIVE</p>
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="col-6 col-lg-2 mb-2 pr-sm-2 pr-0">
          <nuxt-link to="">
            <div class="card landing-card">
              <div class="card-body d-flex align-items-center flex-column">
                <img src="~/assets/img/Games.png" />
                <p class="mb-0 mt-auto">GAMES</p>
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="col-6 col-lg-2 mb-2">
          <div class="card landing-card">
            <div class="card-body d-flex align-items-center flex-column">
              <img
                style="height: 38px; width: auto"
                src="~/assets/img/Virtual.png"
              />
              <p class="mb-0 mt-auto">VIRTUAL</p>
            </div>
          </div>
        </div>
        <div class="col-6 col-lg-2 mb-2 pr-sm-2 pr-0">
          <nuxt-link to="">
            <div class="card landing-card">
              <div class="card-body d-flex align-items-center flex-column">
                <img src="~/assets/img/Casino.png" />
                <p class="mb-0 mt-auto">CASINO</p>
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="col-6 col-lg-2">
          <nuxt-link to="">
            <div class="card landing-card">
              <div class="card-body px-2 d-flex align-items-center flex-column">
                <img src="~/assets/img/Lucky-balls.png" />
                <p class="mt-auto mb-0">LUCKY BALLS</p>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>

      <Highlights />
      <div class="casino">
        <div class="px-0 col-12 mb-1 mt-3">
          <nuxt-link
            to="/"
            id=""
            class="btn bg-black border-white text-uppercase font-weight-bold"
            href="#"
            role="button"
            style="color: #fea62b; font-size: 13px"
            >Top Casino Games</nuxt-link
          >
        </div>

        <div class="container-fluid bottom mb-5">
          <div class="row">
            <div class="scrollcards">
              <div class="card">
                <img
                  class="card-img-top"
                  src="~/assets/img/nams.png"
                  alt=""
                  style="height: 170px; object-fit: "
                />
              </div>
              <div class="card">
                <img
                  class="card-img-top"
                  src="~/assets/img/mani.png"
                  alt=""
                  style="height: 170px; object-fit: cover"
                />
              </div>

              <div class="card">
                <img
                  class="card-img-top"
                  src="~/assets/img/male-dealer.png"
                  alt=""
                  style="height: 170px; object-fit: cover"
                />
              </div>
              <div class="card">
                <img
                  class="card-img-top"
                  src="~/assets/img/640x300.jpg"
                  alt=""
                  style="height: 170px; object-fit: cover"
                />
              </div>

              <div class="card">
                <img
                  class="card-img-top"
                  src="~/assets/img/600x364.jpg"
                  alt=""
                  style="height: 170px; object-fit: cover"
                />
              </div>
              <div class="card">
                <img
                  class="card-img-top"
                  src="~/assets/img/Firebird-Spirit_667x414.png"
                  alt=""
                  style="height: 170px; object-fit: cover"
                />
              </div>

              <div class="card">
                <img
                  class="card-img-top"
                  src="~/assets/img/rocketman.png"
                  alt=""
                  style="height: 170px; object-fit: cover"
                />
              </div>
              <div class="card">
                <img
                  class="card-img-top"
                  src="https://cdn-plat.apidigi.com/plat/prd/Img/partners/1102/banner/Casino_Game_4.png"
                  alt=""
                  style="height: 170px; object-fit: cover"
                />
              </div>



            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Highlights from "~/components/Highlights";
export default {
  components: { Highlights },
  name: "home",
  layout: "default",

  data() {
    return {
      slide: 0,
      sliding: null,
      slickOptions: {
        dots: true,
        focusOnSelect: true,
        infinite: true,
        speed: 500,
        slidesToShow: 3,
        slidesToScroll: 3,
        touchThreshold: 5,
      },
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    },
  },
};
</script>

<style>
.carousel-wrapper {
  padding: 0px 0px;
}
.img-wrapper img {
  margin: auto;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(gray 100%, transparent 0);
}

.body-section {
  margin-top: -50px;
}

@media screen and (max-width: 600px) {
  .body-section {
    margin-top: -25px;
  }

  .carousel .carousel-inner .carousel-item img {
    min-height: 500px;
    object-fit: cover;
    /* object-position: 10px 50px ; */
  }
}

.carousel .carousel-inner .carousel-item img {
  height: 500px;
  object-fit: cover;
  /* object-position: 10px 50px ; */
}

.bg-black {
  background: #000;
}

.tl_games_slider_game img {
  height: 320px;
  width: 100%;
  object-fit: cover;
}

.landing-card {
  background-color: #333;
  color: white;
  height: 120px;
  border: none !important;
}

.landing-card img {
  width: 50px;
}

.bottom {
  margin-top: 40px;
}

.highlight-card.card {
  border: 2px solid #f9a329;
  margin: 10px 4px;
  transition: 0.6s ease;
}
.card {
  border: none;
  margin: 10px 20px 10px 0;
  transition: 0.6s ease;
}

.card:hover {
  transform: scale(1.05);
}

.card-block {
  padding: 10px;
}

.scrollcards {
  /* background-color: #fff; */
  overflow: auto;
  white-space: nowrap;
}

::-webkit-scrollbar {
  width: 0px;
  height: 0px;
  background: transparent;
}

div.scrollcards .card {
  display: inline-block;
  height: 170px;
  width: 350px;
}
</style>
