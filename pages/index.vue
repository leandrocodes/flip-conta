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
      <h2 class="subtitle is-size-5-mobile has-text-right-desktop has-text-centered-mobile">
        Oferecemos as
        <br />
        <span class="is-size-7-mobile">melhores soluções para sua empresa</span>
      </h2>
      <div v-swiper:mySwiper="swiperOption">
        <div class="swiper-wrapper">
          <div class="swiper-slide columns is-centered is-mobile" v-for="banner in banners" :key="banner.text">
            <div class="column is-10-desktop is-6-mobile has-text-centered">
              <img :src="`${banner.img}`" width="65px" />
              <p>
                {{banner.text}}
                <br />
                <strong>{{banner.boldtext}}</strong>
              </p>
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
    <section class="gestao">
      <div class="container">
        <div class="columns is-mobile is-multiline is-variable is-8">
          <div class="column is-6-desktop is-12-mobile">
            <img src="img/gestao-completa.png" alt srcset />
          </div>
          <div class="column is-5-desktop is-12-mobile">
            <div class="texto">
              <h3 class="has-text-info is-size-3 has-text-weight-bold">Uma gestão completa para sua empresa.</h3>

              <p
                class="has-text-grey-darker has-text-weight-semibold"
              >Somos um gerenciador completo no mercado com tudo o que você precisa para a sua empresa.</p>

              <div class="box">
                <div class="icon-box">
                  <font-awesome-icon :icon="['fas', 'check-double']" />
                </div>
                <p class="has-text-info is-size-5 has-text-weight-bold">Gestão completa financeira</p>
              </div>
              <div class="box">
                <div class="icon-box">
                  <font-awesome-icon :icon="['fas', 'check-double']" />
                </div>
                <p class="has-text-info is-size-5 has-text-weight-bold">Gestão completa financeira</p>
              </div>
              <div class="box">
                <div class="icon-box">
                  <font-awesome-icon :icon="['fas', 'check-double']" />
                </div>
                <p class="has-text-info is-size-5 has-text-weight-bold">Gestão completa financeira</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <prices></prices>

    <rodape></rodape>
  </div>
</template>

<script>
import BarraMenuPrimaria from '~/components/barra-menu-primaria.vue'
import prices from '~/components/prices'
import rodape from '~/components/rodape'
export default {
  components: {
    BarraMenuPrimaria,
    prices,
    rodape
  },
  data() {
    return {
      indexImage: 1,
      banners: [{ img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/calendário.png', text: 'cobrança', boldtext: 'recorrente' },
      { img: 'img/nf.png', text: 'nota fiscal de', boldtext: 'serviço' },
      { img: 'img/api.png', text: 'integração via', boldtext: 'API' },
      { img: 'img/segurança.png', text: 'seus pagamentos', boldtext: 'on-line protegidos' },
      { img: 'img/calculadora.png', text: 'juros e ', boldtext: 'multas' }],
      swiperOption: {
        slidesPerView: 6,
        centeredSlides: false,
        clickable: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  },
  created() {
    if (this.$device.isMobile) {
      this.swiperOption.slidesPerView = 1
      this.swiperOption.centeredSlides = false
    }
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
