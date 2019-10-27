<template>
  <section class="hero is-primary is-large home">
    <div class="hero-head">
      <barra-menu></barra-menu>
    </div>

    <div class="hero-body">
      <p class="title">FLIPCONTA</p>
      <p class="subtitle">
        Lorem ipsum dolor
        <strong>sit amet</strong>.
      </p>
      <img src="../assets/img/float-icons.webp" class="anim" />
      <div class="slider-hero">
        <img src="../assets/img/modelo.png" />
      </div>
    </div>
  </section>
</template>

<script>
import BarraMenu from '~/components/barra-menu.vue'

export default {
  components: {
    BarraMenu
  },
  data() {
    return {

    }
  }
}
</script>

<style>
</style>
