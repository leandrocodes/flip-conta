<template>
  <section class="slider">
    <div v-swiper:mySwiper="swiperOption">
      <div class="swiper-wrapper">
        <div class="swiper-slide columns is-centered is-mobile" v-for="slider in pricesSliders" :key="slider.text">
          <div class="column is-8-desktop is-8-mobile has-text-centered">
            <img :src="`${slider.img}`" class="imgTest" width="70px" />
            <!-- <div class="imgTest" v-bind:style="{ backgroundImage: 'url(' + slider.img + ')' }"></div> -->
            <!-- <div id="imgSlider" :style="`background-image: ${slider.background}`"> 
            </div>-->
            <h4 class="is-size-4 has-text-weight-bold has-text-dark">{{ slider.title }}</h4>
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

    <div class="svgs" style="display: none;"></div>
  </section>
</template>

<script>
import svg from '~/static/img/id.svg'
export default {
  data() {
    return {
      svg,
      pricesSliders: [
        { img: "img/id.svg", title: 'Você indica um cliente' },
        { img: 'img/re.svg', title: 'O cliente cadastra na Flipconta' },
        { img: 'img/sc.svg', title: 'O cliente gera o boleto' },
        { img: 'img/de.svg', title: 'O boleto é pago' },
        { img: 'img/cd.svg', title: 'E você recebe a cada boleto' },
      ],
      swiperOption: {
        slidesPerView: 5,
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
.swiper-container {
  width: 100%;
}

.swiper-wrapper {
  display: flex !important;
  justify-content: space-around !important;
  align-items: center !important;
}

.columns {
  margin-top: 15px;
  .column {
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    height: 350px;
    padding: 5%;
    background: white;
    margin: 10px;
    border-radius: 10px;
    box-shadow: 2px 1.5px 5px 2px rgba(0, 0, 0, 0.15);
    img {
      margin-bottom: 2.25em;
    }
    &:hover{
      background: #6712bd;
      h4{
        color: white!important;
      }
      img{
        filter: brightness(0) invert(1);
      }
    }
  }
}
</style>