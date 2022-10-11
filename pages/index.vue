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
      <b-carousel-slide
        img-src="~/assets/img/wop.png"
      ></b-carousel-slide>

      <b-carousel-slide img-src="~/assets/img/wop-2.png">
      </b-carousel-slide>

      <b-carousel-slide img-src="~/assets/img/wop-3.png">
      </b-carousel-slide>

    </b-carousel>

    <div class="container-fluid px-4 body-section">

      <div class="row mb-4">
        <div class="col-6 col-lg-2 mb-2 pr-sm-2 pr-0">
          <nuxt-link to="">
            <div class="card landing-card">
              <div class="card-body  d-flex align-items-center flex-column">
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
        <div class="px-0  col-12 mb-3">
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
        <div class="d-none row justify-content-center mb-3">
          <div class="col-lg-4 col-12 mb-3">
            <nuxt-link to="/" class="tl_games_slider_game">
              <div class="card border-0 rounded-3">
                <img
                  class="card-img-top"
                  src="~/assets/img/spaceman.png"
                  alt=""
                />
              </div>
            </nuxt-link>
          </div>
          <div class="col-lg-4 col-12 mb-3">
            <nuxt-link to="/" class="tl_games_slider_game">
              <div class="card border-0 rounded-3">
                <img

                  src="~/assets/img/rocketman.png"
                  alt=""
                />
              </div>
            </nuxt-link>
          </div>
          <div class="col-lg-4 col-12 mb-3">
            <nuxt-link to="/" class="tl_games_slider_game">
              <div class="card border-0 rounded-3">
                <img
                  class="card-img-top"
                  src="https://cdn-plat.apidigi.com/plat/prd/Img/partners/1102/banner/Casino_Game_4.png"
                  alt=""
                />
              </div>
            </nuxt-link>
          </div>
        </div>

              <div class="row mb-3 ">
        <div class="col-md-4 col-lg-4">
          <nuxt-link to="/" class="tl_landing_banner">
            <div class="card border-0 rounded-3">
              <img
                class="card-img-top"
                src="~/assets/img/pol.gif"
                alt=""
                style="height: 170px; object-fit: cover"
              />
            </div>
          </nuxt-link>
        </div>
        <div class="col-md-4 col-lg-4">
          <nuxt-link to="/" class="">
            <div
              class="card border-0 rounded-3"
              
            >
              <img
                class="card-img-top"
                src="~/assets/img/nams.png"
                alt=""
                style="height: 170px; object-fit: "
              />
            </div>
          </nuxt-link>
        </div>
        <div class="col-md-4 col-lg-4">
          <nuxt-link to="/" class="tl_landing_banner">
            <div
              class="card border-0 rounded-3"
              
            >
              <img
                class="card-img-top"
                src="~/assets/img/mani.png"
                alt=""
                style="height: 170px; object-fit: cover"
              />
            </div>
          </nuxt-link>
        </div>
      </div>

      </div>
    </div>
  </div>
</template>

<script>
import Highlights from '~/components/Highlights'
export default {
  components: { Highlights },
  name: 'home',
  layout: 'default',

  data() {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods:{
    onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
  }
}
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

.body-section{
  margin-top: -50px
}


@media screen and (max-width: 800px) {
  .body-section{
    margin-top: -225px
  }
}


.bg-black {
  background: #000;
}

.tl_games_slider_game img
{
  height: 320px;
  width: 100%;
  object-fit: cover;
}

.landing-card {
  background-color: #333;
  color: white;
  height: 120px;
}

.landing-card img {
  width: 50px;
}



</style>
