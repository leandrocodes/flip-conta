<template>
  <div class = "home">
    <section class="hero is-primary is-large">
      <div class="hero-head">
        <barra-menu-primaria></barra-menu-primaria>
      </div>

      <div class="hero-body">
        <div class="texto-entrada has-text-align-right">
          <h1 class="title has-text-link is-size-1-fullhd">bem-vindo,</h1>
          <h3 class="subtitle has-text-link">
            nós somos a
            <span>flip</span>conta
          </h3>
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
      <h2 class="subtitle has-text-right">Confira nossas soluções</h2>
      <div class="columns is-mobile has-text-centered is-centered">
         <div class="column is-2">
        <div>
          <img src="../assets/img/boleto.png" width="100px" />
          <p>
            o o menor custo para
            <br />
            <strong class="has-text-grey-dark">boleto registrado</strong>
          </p>
        </div>
      </div>
      <div class="column is-2">
        <div>
          <img src="../assets/img/boleto.png" width="100px" />
          <p>
            o o menor custo para
            <br />
            <strong class="has-text-grey-dark">boleto registrado</strong>
          </p>
        </div>
      </div>
      <div class="column is-2">
        <div>
          <img src="../assets/img/boleto.png" width="100px" />
          <p>
            o o menor custo para
            <br />
            <strong class="has-text-grey-dark">boleto registrado</strong>
          </p>
        </div>
      </div>
      <div class="column is-2">
        <div>
          <img src="../assets/img/boleto.png" width="100px" />
          <p>
            o o menor custo para
            <br />
            <strong class="has-text-grey-dark">boleto registrado</strong>
          </p>
        </div>
      </div>
      <div class="column is-2">
        <div>
          <img src="../assets/img/boleto.png" width="100px" />
          <p>
            o o menor custo para
            <br />
            <strong class="has-text-grey-dark">boleto registrado</strong>
          </p>
        </div>
      </div>
      <div class="column is-2">
        <div>
          <img src="../assets/img/boleto.png" width="100px" />
          <p>
            o o menor custo para
            <br />
            <strong class="has-text-grey-dark">boleto registrado</strong>
          </p>
        </div>
      </div>
    </div>
      </div>
  </div>
</template>

<script>
import BarraMenuPrimaria from '~/components/barra-menu-primaria.vue'

export default {
  components: {
    BarraMenuPrimaria
  },
  data() {
    return {
      indexImage: 1
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
    }
  }
}
</script>

<style lang="scss">
</style>
