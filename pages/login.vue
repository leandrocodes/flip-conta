<template>
  <div class="cadastro-fisica">
    <section class="hero is-bold">
      <div class="hero-head">
        <barra-menu-terciaria></barra-menu-terciaria>
      </div>
      <div class="hero-body">
        <p class="subtitle is-6 has-text-centered-mobile">
          você está em >>
          <strong>área de login</strong>
          <!-- Colocar no media -->
        </p>
      </div>
    </section>
    <div class="conteudo">
      <div v-if="fisica" class="columns is-centered is-mobile">
        <div class="column is-9-mobile is-6-tablet is-3-desktop is-3-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Cliente</h4>
          </div>
          <form>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu email" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="password" placeholder="Insira sua senha" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href class="button is-primary is-rounded">Login</a>
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <nuxt-link to="/esqueci" class="has-text-primary">Esqueci a minha senha</nuxt-link>
              </div>
            </div>
          </form>
        </div>
      </div>
      <div v-else class="columns is-centered is-mobile">
        <div class="column is-9-mobile is-6-tablet is-3-desktop is-3-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Consultor</h4>
          </div>
          <form>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu email" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="password" placeholder="Insira sua senha" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href class="button is-primary is-rounded">Login</a>
              </div>
            </div>

            <div class="field">
              <div class="control is-expanded">
                <nuxt-link to="/esqueci" class="has-text-primary">Esqueci a minha senha</nuxt-link>
              </div>
            </div>
          </form>
        </div>
      </div>

      <div class="modelo-bg">
        <img src="~@/assets/img/modelo-cliente.png" alt />
      </div>
      <div class="tabs">
        <div class="tab has-text-weight-semibold" @click="fisica=true" :class="{active: fisica}">Cliente</div>
        <div class="tab has-text-weight-semibold" @click="fisica=false" :class="{active: !fisica}">Consultor</div>
      </div>
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
  data() {
    return {
      fisica: true
    }
  }
}
</script>

<style>
</style>