<template>
  <section class="hero is-primary is-large home">
    <div class="hero-head">
      <barra-menu-primaria></barra-menu-primaria>
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
import BarraMenuPrimaria from '~/components/barra-menu-secundaria.vue'

export default {
  components: {
    BarraMenuPrimaria
  },
  data() {
    return {

    }
  }
}
</script>

<style>
</style>
