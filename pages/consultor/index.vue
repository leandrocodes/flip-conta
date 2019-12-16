<template>
  <div class="consultor">
    <section class="hero is-primary is-large">
      <div class="hero-head">
        <barra-menu-primaria></barra-menu-primaria>
      </div>

      <div class="hero-body">
        <!--         <div class="texto-entrada has-text-centered-mobile-only">
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
              <h1 class="title has-text-link is-size-1-fullhd">bem-vindo,</h1>
              <h2 class="subtitle has-text-success">
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
            <div v-if="indexImage == 3" class="texto-a">
              <h1 class="title has-text-dark is-size-1-fullhd">bem-vindo,</h1>
              <h2 class="subtitle has-text-danger">
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
        </div>-->
        <div class="slider-hero">
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 1" src="@/assets/img/consultor-teste.png" />
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 2" src="@/assets/img/consultor-teste.png" />
          </transition>
          <transition enter-active-class="animated bounceInLeft" leave-active-class="animated bounceOutRight" mode="out-in">
            <img v-if="indexImage == 3" src="@/assets/img/consultor-teste.png" />
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

    <div class="container is-fluid">
      <div class="cards" id="solutions">
        <div v-swiper:mySwiper="swiperOption">
          <div class="swiper-wrapper">
            <div class="swiper-slide columns is-centered is-mobile" v-for="banner in banners" :key="banner.text">
              <div @click="modal = banner.modal" class="swiper-z column is-12-desktop is-8-mobile has-text-centered">
                <div class="texto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, aperiam.</div>
                <div class="data">
                  <img :src="`${banner.img}`" width="65px" height="65px" />
                  <p>
                    {{banner.text}}
                    <br />
                    <strong>{{banner.boldtext}}</strong>
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="swiper-pagination"></div>
          <div v-show="$device.isMobile || $device.isTablet" class="swiper-button-prev">
            <font-awesome-icon :icon="['fas', 'angle-left']" />
          </div>
          <div v-show="$device.isMobile || $device.isTablet" class="swiper-button-next">
            <font-awesome-icon :icon="['fas', 'angle-right']" />
          </div>
        </div>
      </div>
    </div>

    <section class="how-works">
      <div class="container">
        <h3 class="is-size-3 has-text-grey-darker has-text-weight-medium is-uppercase has-text-centered">
          Como
          <span class="has-text-weight-bold">funciona!</span>
        </h3>
        <p
          class="has-text-grey has-text-centered"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda sunt minima eos officiis odit dolores cum magni. Voluptas, eum veritatis.</p>
        <div class="dash-gradient"></div>
      </div>
      <how-works></how-works>
    </section>

    <div class="container" style="margin-top: 5em;">
      <div class="column is-12-desktop is-12-full-hd is-12-widescreen is-12-mobile is-12-tablet indication-pic">
        <img src="~@/assets/img/indicacao.png" alt srcset />
        <div class="card-txt1">
          <h4 class="has-text-weight-bold is-size-4 is-uppercase">agora é só sombra e água fresca!!!</h4>
          <p>
            Agora é descansar
            <br />e esperar a minha conta engordar!!! 😏🤑
          </p>
        </div>
        <div class="card-txt2">
          <h4 class="has-text-weight-bold is-size-4 is-uppercase">Vida boa é assim!!!</h4>
          <p>
            Agora é deixa que a Flipconta
            <br />trabalhe por mim... 😏🤑
          </p>
        </div>
      </div>
    </div>

    <transition name="fade">
      <div v-if="modal == 'indicaCliente'" class="modal is-active">
        <div class="modal-background" @click="modal = ''"></div>
        <div class="modal-content">
          <div class="card">
            <h3 class="has-text-primary is-size-3">
              Olá,
              <strong class="has-text-primary">Charles</strong> seu link foi gerado e você já pode enviar para o seu cliente.
            </h3>
            <p class="is-size-5 has-text-dark" style="margin: 1em 0;">Compartilhe o link do seu convite</p>
            <div class="field has-addons">
              <div class="control" style="width: 100%;">
                <input class="input has-text-grey" type="text" value="www.flipconta.com/indicacao/charles001" />
              </div>
              <div class="control">
                <a class="button is-inverted is-primary">Copiar</a>
              </div>
              <a href="#facebook" class="fb-link button is-rounded social">
                <font-awesome-icon :icon="['fab', 'facebook-messenger']" />
              </a>
              <a href="#twitter" class="twt-link button is-rounded social">
                <font-awesome-icon :icon="['fab', 'whatsapp']" />
              </a>
            </div>
            <p class="is-size-5 has-text-dark" style="margin: 1em 0;">Ou envie o link usando o email do seu cliente</p>
            <div class="field has-addons">
              <div class="control" style="width: 100%;">
                <input class="input has-text-grey" type="text" value="vmaisresultado@gmail.com" />
              </div>
              <div class="control">
                <a class="button is-primary">Enviar convite</a>
              </div>
            </div>
          </div>
        </div>
        <button @click="modal = ''" class="modal-close is-large" aria-label="close"></button>
      </div>
    </transition>

    <transition name="fade">
      <div v-if="modal == 'videoYT'" class="modal is-active">
        <div class="modal-background" @click="modal = ''"></div>
        <div class="modal-content" style="width:50vw; height: 60vh;">
          <div class="video" style="width:50vw; height: 60vh;">
            <iframe
              style="width:50vw; height: 60vh;"
              width="1280"
              height="50rem"
              src="https://www.youtube.com/embed/wQcchdeS4QY"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </div>
        <button @click="modal = ''" class="modal-close is-large" aria-label="close"></button>
      </div>
    </transition>

    <rodape style="margin-top: 5em;"></rodape>
  </div>
</template>

<script>
import BarraMenuPrimaria from '~/components/barra-consultor.vue'
import BarraMenuSecundaria from '~/components/barra-menu-secundaria.vue'
import rodape from '~/components/rodape'
import howWorks from '~/components/how-works'
export default {
  components: {
    BarraMenuPrimaria,
    BarraMenuSecundaria,
    rodape,
    howWorks,
  },
  data() {
    return {
      modal: '',
      indexImage: 1,
      banners: [{ img: 'img/cadastro.png', text: 'cadastre-se', boldtext: 'agora', modal: '' },
      { img: 'img/indica-cliente.png', text: 'indicar um', boldtext: 'cliente', modal: 'indicaCliente' },
      { img: 'img/pdf.png', text: 'baixar o', boldtext: 'mediakit', modal: '' },
      { img: 'img/play-video.png', text: 'assistir o', boldtext: 'nosso vídeo', modal: 'videoYT' }],
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
      this.swiperOption.centeredSlides = true
    }
    if (this.$device.isTablet) {
      this.swiperOption.slidesPerView = 1
      this.swiperOption.centeredSlides = true
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
.modal {
  @media screen and (min-width: 320px) and (max-width: 425px) {
    .modal-content {
      width: 100vw !important;
      .video {
        width: 100vw !important;
        iframe {
          width: 100vw !important;
        }
      }
    }
  }
  .card {
    padding: 5em;
    border-radius: 10px;
    iframe {
    }
  }
  .field {
    display: flex;
    align-items: center;
    .input {
      border: black;
    }
  }
  .fb-link {
    background-color: #0084ff;
    color: white;
    width: 2.75em;
    height: 2.75em;
    font-size: 1.25em;
  }
  .twt-link {
    background-color: #14d110;
    color: white;
    width: 2.75em;
    height: 2.75em;
    font-size: 1.25em;
  }
  .control {
    .button {
      background-color: #519399;
      font-weight: bold;
      transition: background-color 0.1s ease-in-out;
      &:hover {
        background-color: #406c70;
      }
      &.is-inverted {
        background-color: transparent;
        color: #519399;
        transition: background-color color 0.1s ease-in-out;
        &:hover {
          color: #406c70;
          background-color: #f5f5f5;
        }
      }
    }
  }
}
.fade-enter-active,
.fade-leave-active {
  transition: all 0.2s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
