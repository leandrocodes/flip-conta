<template>
  <!-- You can find this swiper instance object in current component by the "mySwiper"  -->
  <div v-swiper:mySwiper="swiperOption">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="banner in banners" :key="banner">
        <img :src="`${banner.img}`" width="100px" />
        <p>{{banner.text}}</p>
      </div>
    </div>
    <!-- <div class="swiper-pagination"></div> -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      banners: [{ img: 'img/boleto.png', text: 'boleto' },
      { img: 'img/boleto.png', text: 'boleto' },
      { img: 'img/boleto.png', text: 'boleto' }],
      swiperOption: {
        slidesPerView: 6,
        centeredSlides: true,
        spaceBetween: 30,
        clickable: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  },
  mounted () {
    setTimeout(() => {
      this.banners.push({ img: 'img/boleto.png', text: 'boleto' })
      console.log('banners update')
    }, 3000)
    this.mySwiper.slideTo(3, 1000, false)
  }
}
</script>


<style lang="scss" scoped>
.my-swiper {
  height: 300px;
  width: 100%;
  .swiper-slide {
    text-align: center;
    font-size: 38px;
    font-weight: 700;
    background-color: #eee;
  }
  .swiper-pagination {
    > .swiper-button-next {
      color: red;
    }
  }
}
</style>