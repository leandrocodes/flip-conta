<template>
  <!-- You can find this swiper instance object in current component by the "mySwiper"  -->
  <div v-swiper:mySwiper="swiperOption">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="banner in banners" :key="banner">
        <img :src="banner" />
      </div>
    </div>
    <div class="swiper-pagination"></div>
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      banners: ['https://images.pexels.com/photos/2534475/pexels-photo-2534475.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260',
        'https://images.pexels.com/photos/2534475/pexels-photo-2534475.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260',
        'https://images.pexels.com/photos/2534475/pexels-photo-2534475.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'],
      swiperOption: {
        clickable: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  },
  mounted() {
    setTimeout(() => {
      this.banners.push('/4.jpg')
      console.log('banners update')
    }, 3000)
    console.log(
      'This is current swiper instance object', this.mySwiper,
      'It will slideTo banners 3')
    this.mySwiper.slideTo(3, 1000, false)
  }
}
</script>


<style lang="scss" scoped>
img {
  display: block;
  width: 400px;
  margin: 0 auto;
}
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
    > .swiper-pagination-bullet {
      background-color: red;
    }
  }
}
</style>