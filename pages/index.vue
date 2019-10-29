<template>
  <div class="home">
    <section class="hero is-primary is-large">
      <div class="hero-head">
        <barra-menu-primaria></barra-menu-primaria>
      </div>

      <div class="hero-body">
        <div class="texto-entrada has-text-align-right">
          <h1 class="title has-text-link is-size-1-fullhd">bem-vindo,</h1>
          <h2 class="subtitle has-text-link">
            nós somos a
            <span>flip</span>conta
          </h2>
        </div>
        <img src="../assets/img/float-icons.webp" class="anim" />
        <div class="slider-hero">
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 1" src="../assets/img/modelo.png" />
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 2" src="../assets/img/modelo2.png" />
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 3" src="../assets/img/modelo2.png" />
          </transition>
        </div>
        <div class="nav-buttons">
          <a class="button is-rounded is-primary is-outlined" @click="sliderImage('frente')">
            <font-awesome-icon :icon="['fas', 'angle-left']" />
          </a>
          <a class="button is-rounded is-primary is-outlined" @click="sliderImage('tras')">
            <font-awesome-icon :icon="['fas', 'angle-right']" />
          </a>
        </div>
      </div>
    </section>

    <div class="cards">
      <h2 class="subtitle has-text-right-desktop has-text-centered-mobile">
        Oferecemos as
        <br />
        <span>melhores soluções para sua empresa</span>
      </h2>
      <div v-swiper:mySwiper="swiperOption">
        <div class="swiper-wrapper">
          <div class="swiper-slide columns is-centered is-mobile" v-for="banner in banners" :key="banner.text">
            <div class="column has-text-centered">
              <img :src="`${banner.img}`" width="100px" />
              <p>
                {{banner.text}}
                <br />
                <strong>{{banner.boldtext}}</strong>
              </p>
            </div>
          </div>
        </div>
        <div class="swiper-pagination"></div>
        <div class="swiper-button-prev">
          <font-awesome-icon :icon="['fas', 'angle-left']" />
        </div>
        <div class="swiper-button-next">
          <font-awesome-icon :icon="['fas', 'angle-right']" />
        </div>
      </div>
    </div>
    <prices></prices>
  </div>
</template>

<script>
import BarraMenuPrimaria from '~/components/barra-menu-primaria.vue'
import prices from '~/components/prices'
export default {
  components: {
    BarraMenuPrimaria,
    prices,
  },
  data () {
    return {
      indexImage: 1,
      banners: [{ img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' }],
      swiperOption: {
        slidesPerView: 6,
        centeredSlides: true,
        clickable: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  },
  created () {
    if (this.$device.isMobile) {
      this.swiperOption.slidesPerView = 2
      this.swiperOption.centeredSlides = false
    }
  },
  methods: {
    sliderImage (val) {
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
  }
}
</script>

<style lang="scss">
.cards {
  .swiper-wrapper {
    width: 80%;
  }
}
.cards {
  width: 100vw;
  .subtitle {
    margin-right: 15em;
  }
}
</style>
