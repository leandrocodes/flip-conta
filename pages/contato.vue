<template>
  <div class="contact">
    <section class="hero is-primary is-bold">
      <div class="hero-head">
        <barra-menu-secundaria></barra-menu-secundaria>
      </div>
      <div class="hero-body">
        <p class="subtitle is-6">
          VOCÊ ESTÁ EM >>
          <strong>CONTATO</strong>
        </p>
      </div>
    </section>
    <div class="columns first is-centered is-mobile">
      <div class="column is-10-mobile is-8-tablet is-4-desktop is-3-fullhd">
        <div class="texto-inicio has-text-centered">
          <h1 class="title has-text-primary has-text-weight-bold">Fale Conosco</h1>
          <h3 class="subtitle has-text-weight-semibold">Tire dúvidas, elogios e mais</h3>
        </div>
        <form>
          <div class="field is-grouped is-grouped-centered">
            <div class="control is-expanded">
              <input class="input" type="text" placeholder="Nome" />
            </div>
            <div class="control is-expanded">
              <input class="input" type="text" placeholder="Email" />
            </div>
          </div>
          <div class="field is-grouped is-grouped-centered">
            <div class="control is-expanded">
              <input class="input" type="text" placeholder="Celular" />
            </div>
            <div class="control is-expanded">
              <input class="input" type="text" placeholder="Assunto" />
            </div>
          </div>
          <div class="field">
            <div class="control is-expanded">
              <textarea class="textarea" placeholder="Sua Mensagem"></textarea>
            </div>
          </div>
          <div class="field">
            <div class="control">
              <a href class="button is-link is-rounded">Enviar Mensagem</a>
            </div>
          </div>
        </form>
      </div>
    </div>

    <div class="columns second has-text-centered is-centered is-mobile is-multline ">
      
      <div class="column is-10-mobile is-8-tablet is-2-desktop">
        <div class="circle">
          <font-awesome-icon :icon="['fas', 'envelope']" />
        </div>
        <h1 class="title  has-text-black has-text-weight-bold">Email</h1>
        <h2 class="subtitle has-text-weight-semibold">admin@evolta.com</h2>
        <h2 class="subtitle has-text-weight-semibold">info@evolta.com</h2>
      </div>
      <div class="column is-10-mobile is-8-tablet is-2-desktop">
        <div class="circle">
          <font-awesome-icon :icon="['fas', 'map-marker-alt']" />
        </div>
        <h1 class="title has-text-black has-text-weight-bold">Localização</h1>
        <h2 class="subtitle has-text-weight-semibold">2750 Quadra Steet Victoria, New York</h2>
        <h2 class="subtitle has-text-weight-semibold">USA</h2>
      </div>
      <div class="column is-10-mobile is-8-tablet is-2-desktop">
        <div class="circle">
          <font-awesome-icon :icon="['fas', 'phone-alt']" />
        </div>
        <h1 class="title has-text-black has-text-weight-bold">Telefone</h1>
        <h2 class="subtitle has-text-weight-semibold">(99) 99999 9999</h2>
        <h2 class="subtitle has-text-weight-semibold">(99) 99999 9999</h2>
      </div>

    </div>

  </div>

</template>

<script>

import BarraMenuSecundaria from '~/components/barra-menu-secundaria.vue'

export default {
  components: {
    BarraMenuSecundaria
  },
  data() {
    return {

    }
  }
}
</script>

<style>
</style>