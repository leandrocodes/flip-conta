<template>
  <section class="precos">
    <h2 class="is-size-3 has-text-weight-bold has-text-centered has-text-white">taxas simples e transparentes</h2>
    <p
      class="is-size-5 has-text-weight-normal has-text-centered has-text-light"
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
      <div v-show="$device.isMobile" class="swiper-button-prev">
        <font-awesome-icon :icon="['fas', 'angle-left']" />
      </div>
      <div v-show="$device.isMobile" class="swiper-button-next">
        <font-awesome-icon :icon="['fas', 'angle-right']" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      banners: [{ img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' },
      { img: 'img/boleto.png', text: 'o menor custo para', boldtext: 'boleto registrado' }],
      swiperOption: {
        slidesPerView: 3,
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
  }
}
</script>

<style scoped lang="scss">
.columns {
  margin-top: 15px;
  .column{
      background: white;
      margin: 10px;
      border-radius: 10px;
      box-shadow: 2px 1.5px 5px 2px rgba(0,0,0,0.15);
  }
}

.swiper-container {
  width: 80%;
}
.swiper-wrapper {
  width: 80%;
  .swiper-slide {
    margin: 0 auto;
  }
}
</style>