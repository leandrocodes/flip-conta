<template>
  <section class="precos">
    <h2 class="is-size-3 has-text-weight-bold has-text-centered has-text-light">taxas simples e transparentes</h2>
    <p
      class="is-size-5 has-text-weight-normal has-text-centered has-text-grey-lighter"
    >Você só paga quando recebe, sem mensalidade, taxa de adesão ou manutenção.</p>
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
  </section>
</template>

<script>
export default {
  data () {
    return {
      banners: [{ img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' }],
      swiperOption: {
        slidesPerView: 3,
        centeredSlides: false,
        clickable: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  }
}
</script>

<style>
</style>