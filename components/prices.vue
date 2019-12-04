<template>
  <section class="precos">
    <div class="conteudo">
      <h2 class="is-size-3 has-text-weight-bold has-text-centered has-text-white">taxas simples e transparentes</h2>
      <p
        class="is-size-5 has-text-weight-normal has-text-centered has-text-light"
      >Você só paga quando recebe, sem mensalidade, taxa de adesão ou manutenção.</p>
      <div v-swiper:mySwiper="swiperOption">
        <div class="swiper-wrapper">
          <div class="swiper-slide columns is-centered is-mobile" v-for="slider in pricesSliders" :key="slider.text">
            <div class="column is-8-desktop is-12-mobile has-text-centered">
              <img :src="`${slider.img}`" width="150px" />
              <h4 class="subtitle has-text-weight-bold">{{ slider.title }}</h4>
              <a style="margin-bottom: 10px;" class="button is-info is-rounded has-text-light has-text-weight-semibold">{{ slider.price }}</a>
              <div class="columns is-centered">
                <div class="column is-8" style="box-shadow: none;">
                  <ul class="has-text-left" v-for="topic in slider.topics" :key="topic">
                    <li class="has-text-info">
                      <font-awesome-icon :icon="['fas', 'check-circle']" />
                      {{ topic }}
                    </li>
                  </ul>
                </div>
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
  </section>
</template>

<script>
export default {
  data () {
    return {
      pricesSliders: [
        { img: 'img/price-boleto.png', title: 'boleto bancário', price: 'R$ 1,00', topics: ['por boleto pago', 'sem taxas de emissão', 'receba em 2 dias'] },
        { img: 'img/price-cartao.png', title: 'cartão de crédito', price: 'R$ 1,00', topics: ['por boleto pago', 'sem taxas de emissão', 'receba em 2 dias'] },
        { img: 'img/price-consultor.png', title: 'seja consultor', price: 'R$ 1,00', topics: ['por boleto pago', 'sem taxas de emissão', 'receba em 2 dias'] }
      ],
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
  created () {
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
  .column {
    background: white;
    margin: 10px;
    border-radius: 10px;
    box-shadow: 2px 1.5px 5px 2px rgba(0, 0, 0, 0.15);
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