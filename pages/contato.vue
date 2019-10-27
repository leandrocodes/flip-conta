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
    <div class="columns is-centered is-mobile">
      <div class="column is-10-mobile is-8-tablet is-4-desktop is-3-fullhd">
        <div class="texto-entrada has-text-centered">
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