<template>
  <div class="team-container">
    <Navigation />
    <a class="close-icon" @click="$router.back()">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="40"
        height="40"
        fill="#2D2D2D"
        class="bi bi-x-circle-fill"
        viewBox="0 0 16 16"
      >
        <path
          d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM5.354 4.646a.5.5 0 1 0-.708.708L7.293 8l-2.647 2.646a.5.5 0 0 0 .708.708L8 8.707l2.646 2.647a.5.5 0 0 0 .708-.708L8.707 8l2.647-2.646a.5.5 0 0 0-.708-.708L8 7.293 5.354 4.646z"
        />
      </svg>
    </a>
    <section class="container">
      <div class="team-bar">
        <figure>
          <img src="https://i.imgur.com/G1xKi1b.png" alt="Hugo" />
        </figure>
        <h1 class="name">HUGO V.</h1>
        <p class="puesto">ESTRATEGA DE MARKETING</p>
        <p class="description ab">
          Hugo mercadólogo con 20 años de experiencia en Marketing integral,
          especializado en inteligencia de mercados y creador de un sistema de
          unificación de publicidad y comercialización para marcas y proyectos.
        </p>
        <p class="description ab">
          Hugo también es director del Festival de teatro Galerías con 5
          ediciones y director de teatro con 10 años de experiencia.
        </p>
      </div>
      <div class="description">
        <p class="cd">
          Hugo mercadólogo con 20 años de experiencia en Marketing integral,
          especializado en inteligencia de mercados y creador de un sistema de
          unificación de publicidad y comercialización para marcas y proyectos.
        </p>
        <p class="cd">
          Hugo también es director del Festival de teatro Galerías con 5
          ediciones y director de teatro con 10 años de experiencia.
        </p>
        <div class="music">
          <VueSlickCarousel
            v-bind="settings"
            class="carousel-vtrv"
            :arrows="true"
            :dots="false"
            :infinite="true"
            :center-mode="true"
            :slides-to-show="1"
            :slides-to-scroll="1"
            :variable-width="true"
          >
            <div><img src="@/assets/mkt/1.png" alt="" /></div>
            <div><img src="@/assets/mkt/2.png" alt="" /></div>
            <div><img src="@/assets/mkt/3.png" alt="" /></div>
            <div><img src="@/assets/mkt/4.png" alt="" /></div>
            <div><img src="@/assets/mkt/5.png" alt="" /></div>
            <div><img src="@/assets/mkt/6.png" alt="" /></div>
            <div><img src="@/assets/mkt/7.png" alt="" /></div>
          </VueSlickCarousel>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation'
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
  components: {
    Navigation,
    VueSlickCarousel,
  },
  data() {
    return {
      settings: {
        responsive: [
          {
            breakpoint: 480,
            settings: {
              variableWidth: false,
              initialSlide: 7,
            },
          },
        ],
      },
    }
  },
}
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.team-bar {
  background-color: var(--metodologia);
  background-image: url(@/assets/images/logo-mask.png);
  width: 60rem;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column;
  padding: 0 3rem;
}
.name {
  font-family: sifonn;
  font-size: 5rem;
  color: #fff;
  text-transform: uppercase;
  margin-top: 1rem;
}
.puesto {
  font-family: c-gothic;
  font-size: 2.6rem;
  color: #212121;
  text-transform: uppercase;
  margin-top: 3.5rem;
}
.description {
  font-family: c-gothic;
  font-size: 3rem;
  color: #212121;
  box-sizing: content-box;
  width: 60%;
  margin-bottom: 20rem;
}
.ab {
  display: none;
}
.description p {
  margin: 4rem;
}
.close-icon {
  position: absolute;
  right: 0;
  margin: 20px;
}
.music {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.carousel-vtrv {
  width: 60%;
  position: absolute;
  top: 80%;
  left: 35%;
}

/* -------------------------------------------Responsive design */

@media screen and (max-width: 1536px) {
  .video iframe {
    width: 60rem;
    height: 40rem;
  }
  .team-bar {
    width: 50rem;
  }
  .team-bar img {
    width: 25rem;
  }
  .name {
    font-size: 4rem;
  }
  .carousel-vtrv {
    left: 36%;
  }
  .carousel-vtrv img {
    height: 20rem;
  }
  .description {
    font-size: 2.9rem;
  }
  .description p {
    margin: 3rem;
  }
}
@media screen and (max-width: 1440px) {
  .video iframe {
    width: 55rem;
    height: 35rem;
  }
  .carousel-vtrv {
    left: 37%;
  }
  .carousel-vtrv img {
    height: 18rem;
  }
  .description {
    font-size: 2.8rem;
  }
}
@media screen and (max-width: 1366px) {
  .video iframe {
    width: 50rem;
    height: 30rem;
  }
  .carousel-vtrv {
    left: 40%;
    width: 55%;
  }
  .carousel-vtrv img {
    height: 18rem;
  }
  .team-bar {
    width: 45rem;
  }
  .team-bar img {
    width: 20rem;
  }
  .name {
    font-size: 3.5rem;
  }
  .puesto {
    font-size: 2.4rem;
  }
  .description {
    font-size: 2.7rem;
  }
}
@media screen and (max-width: 1280px) {
  .description {
    font-size: 2.2rem;
  }
}
@media screen and (max-width: 1024px) {
  .video iframe {
    width: 45rem;
    height: 25rem;
  }
  .team-bar {
    width: 40rem;
  }
  .puesto {
    font-size: 2rem;
  }
  .carousel-vtrv {
    left: 44%;
    width: 52%;
  }
  .cd {
    padding: 0;
  }
}
@media screen and (max-width: 1000px) {
  .description p {
    margin: 2rem;
  }
  .puesto {
    font-size: 1.8rem;
  }
}
@media screen and (max-width: 830px) {
  .description {
    font-size: 1.5rem;
  }
}
@media screen and (max-width: 768px) {
  .container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column;
  }
  .team-bar {
    width: 100vw;
  }
  .carousel-vtrv {
    left: 5%;
    width: 90%;
    top: 120%;
  }
  .carousel-vtrv img {
    height: 22rem;
  }
  .video {
    margin-top: 5rem;
    margin-bottom: 0;
  }
  .ab {
    display: initial;
    font-family: c-gothic;
    font-size: 1.6rem;
    color: #fff;
    margin-top: 5rem;
    margin-bottom: 0;
    width: auto;
    padding: 0 1rem;
  }
  .cd {
    display: none;
  }
}
@media screen and (max-width: 576px) {
  .carousel-vtrv {
    left: 10%;
    width: 80%;
  }
}
@media screen and (max-width: 540px) {
  .carousel-vtrv {
    left: 11%;
    padding: 0 2rem;
  }
  .carousel-vtrv img {
    height: 19rem;
  }
  .slick-prev,
  .slick-next {
    top: 25%;
  }
}
@media screen and (max-width: 480px) {
}
@media screen and (max-width: 426px) {
  .carousel-vtrv {
    top: 130%;
  }
}
@media screen and (max-width: 376px) {
  .team-bar img {
    width: 18rem;
  }
  .name {
    font-size: 3rem;
  }
  .puesto {
    font-size: 1.8rem;
  }
  .ab {
    font-size: 1.4rem;
  }
}
@media screen and (max-width: 320px) {
  .name {
    font-size: 2.5rem;
  }
  .puesto {
    font-size: 1.6em;
  }
  .team-bar {
    width: 100vw;
    height: 100%;
    padding: 4rem 2rem;
  }
  .carousel-vtrv {
    top: 170%;
  }
}
</style>
