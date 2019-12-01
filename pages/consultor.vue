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
                <br>
                <span class="is-orange has-text-weight-medium">venha ser um <span>consultor</span>!</span>
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
      <a class="button is-rounded is-dark is-outlined" @click="sliderImage('frente')">
        <font-awesome-icon :icon="['fas', 'angle-left']" />
      </a>
      <a class="button is-rounded is-dark is-outlined" @click="sliderImage('tras')">
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
                <img :src="`${banner.img}`" width="65px" height="65px" />
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

    <prices id="prices"></prices>

    <section class="clientes">
      <div class="container is-fluid">
        <div class="columns is-mobile is-centered is-4 is-multiline">
          <div class="column is-6-desktop is-12-monile">
            <h2 class="is-size-3 has-text-weight-bold has-text-left">Quem usa, recomenda</h2>
            <p class="has-text-weight-semibold has-text-left has-text-grey">Potencielize você também no mercado, alguns de nossos clientes.</p>
            <div class="comentarios columns is-mobile is-multiline is-centered">
              <div class="column is-12-mobile comentario 1">
                <img src="img/profile.png" alt class="profile-pic" />
                <div class="txt">
                  <p class="has-text-dark-grey">Vanessa Santos</p>
                  <p class="job">Fitdance</p>
                  <p class="comentario-txt">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates, odit.</p>
                </div>
              </div>
              <div class="column is-12-mobile comentario 2">
                <img src="img/profile.png" alt class="profile-pic" />
                <div class="txt">
                  <p class="has-text-dark-grey">Vanessa Santos</p>
                  <p class="job">Fitdance</p>
                  <p class="comentario-txt">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates, odit.</p>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-4-desktop is-12-mobile">
            <img src="~@/assets/img/clientes.png" />
          </div>
        </div>
      </div>
    </section>

    <section class="nosso-blog">
      <div class="container">
        <h2 class="is-size-2 has-text-weight-bold has-text-centered has-text-success">Nosso blog</h2>
        <p class="has-text-weight-semibold has-text-centered has-text-grey">Dicas valiosas do mercado financeiro</p>
        <div class="columns is-centered is-mobile is-multiline">
          <div class="column is-4-desktop is-8-mobile">
            <div class="green-badge">
              <time datetime="2016-1-1" class="is-size-7 has-text-light">
                Admin / 15 de agosto, 2019
                <span class="is-size-2 has-text-light has-text-right">
                  <font-awesome-icon :icon="['fas', 'thumbtack']" />
                </span>
              </time>
              <h3 class="is-size-4 has-text-white">Lorem ipsum dolor sit amet.</h3>
            </div>
            <div class="card">
              <div class="card-image">
                <figure class="image is-4by3">
                  <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image" />
                </figure>
              </div>
              <div class="card-content">
                <div class="content">
                  <time datetime="2016-1-1" class="is-size-7 has-text-grey">Admin / 15 de agosto, 2019</time>
                  <br />
                  <h3 class="is-size-4 has-text-grey-dark">Lorem ipsum dolor sit amet.</h3>
                  <p class="is-size-6 has-text-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus, blanditiis!</p>
                  <br />
                  <a href class="has-text-weight-bold has-text-grey-dark">
                    Ler mais
                    <span class="has-text-weight-bold has-text-success is-size-4">+</span>
                  </a>
                </div>
              </div>
            </div>
          </div>

          <div class="column is-4-desktop is-8-mobile">
            <div class="card">
              <div class="card-image">
                <figure class="image is-4by3">
                  <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image" />
                </figure>
              </div>
              <div class="card-content">
                <div class="content">
                  <time datetime="2016-1-1" class="is-size-7 has-text-grey">Admin / 15 de agosto, 2019</time>
                  <br />
                  <h3 class="is-size-4 has-text-grey-dark">Lorem ipsum dolor sit amet.</h3>
                  <p class="is-size-6 has-text-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus, blanditiis!</p>
                  <br />
                  <a href class="has-text-weight-bold has-text-grey-dark">
                    Ler mais
                    <span class="has-text-weight-bold has-text-success is-size-4">+</span>
                  </a>
                </div>
              </div>
            </div>
            <div class="brown-badge">
              <time datetime="2016-1-1" class="is-size-7 has-text-light">
                Admin / 15 de agosto, 2019
                <span class="is-size-2 has-text-light has-text-right">
                  <font-awesome-icon :icon="['fas', 'link']" />
                </span>
              </time>
              <h3 class="is-size-4 has-text-white">Lorem ipsum dolor sit amet.</h3>
            </div>
          </div>

          <div class="column is-4-desktop is-8-mobile">
            <div class="grey-badge">
              <time datetime="2016-1-1" class="is-size-7 has-text-light">
                Admin / 15 de agosto, 2019
                <span class="is-size-2 has-text-light has-text-right">
                  <font-awesome-icon :icon="['fas', 'quote-right']" />
                </span>
              </time>
              <h3 class="is-size-4 has-text-white">Lorem ipsum dolor sit amet.</h3>
            </div>
            <div class="card">
              <div class="card-image">
                <figure class="image is-4by3">
                  <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image" />
                </figure>
              </div>
              <div class="card-content">
                <div class="content">
                  <time datetime="2016-1-1" class="is-size-7 has-text-grey">Admin / 15 de agosto, 2019</time>
                  <br />
                  <h3 class="is-size-4 has-text-grey-dark">Lorem ipsum dolor sit amet.</h3>
                  <p class="is-size-6 has-text-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus, blanditiis!</p>
                  <br />
                  <a href class="has-text-weight-bold has-text-grey-dark">
                    Ler mais
                    <span class="has-text-weight-bold has-text-success is-size-4">+</span>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

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
      banners: [{ img: 'img/boleto.png', text: 'cadastre-se', boldtext: 'agora' },
      { img: 'img/calendário.png', text: 'indicar um', boldtext: 'cliente' },
      { img: 'img/nf.png', text: 'baixar o', boldtext: 'mediakit' },
      { img: 'img/calculadora.png', text: 'assistir o', boldtext: 'nosso vídeo' }],
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
