<template>
  <div class="consultor">
    <section class="hero is-primary is-large">
      <div class="hero-head">
        <barra-menu-primaria></barra-menu-primaria>
      </div>

      <div class="hero-body">
        <div class="texto-entrada has-text-align-right">
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="in-out">
            <div v-if="indexImage == 1" class="texto-a">
              <h1 class="title has-text-primary is-size-1-fullhd">bem-vindo,</h1>
              <h2 class="subtitle has-text-primary">
                nós somos a
                <span>flip</span>conta.
                <br />
                <span class="is-orange has-text-weight-medium">
                  venha ser um
                  <span>consultor</span>!
                </span>
              </h2>
            </div>
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="in-out">
            <div v-if="indexImage == 2" class="texto-a">
              <h1 class="title has-text-link is-size-1-fullhd">amet</h1>
              <h2 class="subtitle has-text-link">
                consectetur
                <span>adipisicing</span>elit.
              </h2>
            </div>
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="in-out">
            <div v-if="indexImage == 3" class="texto-a">
              <h1 class="title has-text-link is-size-1-fullhd">lorem,</h1>
              <h2 class="subtitle has-text-link">
                ipsum
                <span>dolor</span>sit
              </h2>
            </div>
          </transition>
        </div>
        <div class="slider-hero">
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 1" src="../assets/img/consultor-teste.png" />
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 2" src="../assets/img/consultor-teste.png" />
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 3" src="../assets/img/consultor-teste.png" />
          </transition>
        </div>
      </div>
    </section>

    <div class="nav-buttons">
      <a class="button is-rounded is-primary is-outlined" @click="sliderImage('frente')">
        <font-awesome-icon :icon="['fas', 'angle-left']" />
      </a>
      <a class="button is-rounded is-primary is-outlined" @click="sliderImage('tras')">
        <font-awesome-icon :icon="['fas', 'angle-right']" />
      </a>
    </div>

    <div class="cards" id="solutions" style="margin-top: 6rem">
      <div v-swiper:mySwiper="swiperOption">
        <div class="swiper-wrapper">
          <div class="swiper-slide columns is-centered is-mobile" v-for="banner in banners" :key="banner.text">
            <div class="swiper-z column is-6-fullhd is-10-desktop is-6-mobile">
              <div class="texto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, aperiam.</div>
              <div class="data">
                <img :src="`${banner.img}`" width="75px" height="75px" />
                <p class="is-size-4">
                  {{banner.text}}
                  <br />
                  <strong>{{banner.boldtext}}</strong>
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="swiper-pagination"></div>
        <div v-show="$device.isMobile" class="swiper-button-prev">
          <font-awesome-icon :icon="['fas', 'angle-left']" />
        </div>
        <div v-show="$device.isMobile" class="swiper-button-next">
          <font-awesome-icon :icon="['fas', 'angle-right']" />
        </div>
      </div>
    </div>

    <rodape></rodape>
  </div>
</template>

<script>
import BarraMenuPrimaria from '~/components/barra-consultor.vue'
import BarraMenuSecundaria from '~/components/barra-menu-secundaria.vue'
import prices from '~/components/prices'
import rodape from '~/components/rodape'
export default {
  components: {
    BarraMenuPrimaria,
    BarraMenuSecundaria,
    prices,
    rodape
  },
  data() {
    return {
      indexImage: 1,
      banners: [{ img: 'img/cadastro.png', text: 'cadastre-se', boldtext: 'agora' },
      { img: 'img/indica-cliente.png', text: 'indicar um', boldtext: 'cliente' },
      { img: 'img/pdf.png', text: 'baixar o', boldtext: 'mediakit' },
      { img: 'img/play-video.png', text: 'assistir o', boldtext: 'nosso vídeo' }],
      swiperOption: {
        slidesPerView: 6,
        centeredSlides: false,
        clickable: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      },
      active: null
    }
  },
  created() {
    if (this.$device.isMobile) {
      this.swiperOption.slidesPerView = 1
      this.swiperOption.centeredSlides = false
    }
  },
  mounted() {
    this.$nextTick(function () {
      window.addEventListener("scroll", function () {
        var navbar = document.getElementById("nav")
        if (document.documentElement.scrollTop >= 150) {
          navbar.style.backgroundColor = 'white'
        } else {
          navbar.style.backgroundColor = 'transparent'
        }
      })
    })
  },
  methods: {
    sliderImage(val) {
      if (val == 'frente') {
        this.indexImage++
        if (this.indexImage > 3)
          this.indexImage = 1
      } else {
        this.indexImage--
        if (this.indexImage < 1)
          this.indexImage = 3
      }
    },
    entrou() {
      this.active = !this.active
      console.log(this.active)
    }
  }
}
</script>

<style lang="scss">
.cards {
  .swiper-wrapper {
    .swiper-slide {
      margin: 0 auto;
    }
  }
}
.cards {
  width: 100vw;
  margin-bottom: 50px;
  .subtitle {
    margin-right: 15em;
  }
}
</style>
