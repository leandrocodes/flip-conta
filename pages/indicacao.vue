<template>
    <section class="hero indication">
      <div class="hero-head">
        <barra-menu-terciaria></barra-menu-terciaria>
      </div>
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-offset-2 is-5 has-text-left">
              <p class="has-text-light">código do convite</p>
              <a class="button is-light has-text-weight-bold">CHARLES101</a>
              <p class="is-size-4 has-text-white has-text-weight-bold"> <span>Charles</span> convidou você <br> para conhecer a flipconta. </p>
              <p class="is-size-4 has-text-white has-text-weight-bold">  uma simplicidade na sua gestão.</p>
              <a class="button is-primary has-text-white has-text-weight-semibold">cadastrar</a>
            </div>
          </div>
        </div>
      </div>
      <div class="modelo-convite">
        <img src="~@/assets/img/modelo_convite.png" alt="" srcset="">
      </div>
    </section>
</template>

<script>
import barraMenuTerciaria from '../components/barra-menu-terciaria.vue'
export default {
  components: {
    barraMenuTerciaria
  }
}
</script>

<style>

</style>