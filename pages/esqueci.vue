<template>
  <div class="login-cliente">
    <section class="hero is-bold">
      <div class="hero-head">
        <barra-menu-terciaria></barra-menu-terciaria>
      </div>
      <div class="hero-body">
        <p class="subtitle is-6 has-text-centered-mobile">
          você está em >>
          <strong>esqueci a senha</strong>
          <!-- Colocar no media -->
        </p>
      </div>
    </section>
    <div class="conteudo">
      <div class="columns is-centered is-mobile">
        <div class="column is-10-mobile is-8-tablet is-3-desktop is-2-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Recuperar conta</h4>
          </div>
          <form>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Digite o e-mail da sua conta" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href class="button is-primary is-rounded">Enviar</a>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
    <div class="modelo-bg">
      <img src="~@/assets/img/modelo-cliente.png" alt />
    </div>
    <rodape></rodape>
  </div>
</template>

<script>

import BarraMenuTerciaria from '~/components/barra-menu-terciaria.vue'
import Rodape from '~/components/rodape.vue'

export default {
  components: {
    BarraMenuTerciaria,
    Rodape
  },
  data () {
    return {
    }
  }
}
</script>

<style>
</style>