<template>
  <div class="login-cliente">
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
      <div v-if="cliente" class="columns is-centered is-mobile">
        <div class="column is-10-mobile is-8-tablet is-3-desktop is-2-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Login do Cliente</h4>
          </div>
          <form>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu email" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira sua senha" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href class="button is-primary is-rounded">Entrar</a>
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href="#" class="ajuda has-text-centered-mobile has-text-weight-semibold">Esqueci a senha</a>
              </div>
            </div>
          </form>
        </div>
      </div>
      <div v-else class="columns is-centered is-mobile">
        <div class="column is-10-mobile is-8-tablet is-3-desktop is-2-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Login do Consultor</h4>
          </div>
          
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu email" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira sua senha" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href class="button is-primary is-rounded">Entrar</a>
              </div>
            </div>
            <div class="field">
              <nuxt-link to="/esqueci" class="ajuda has-text-centered-mobile has-text-weight-semibold">Esqueci a senha</nuxt-link>
            </div>
        </div>
      </div>
    </div>
    <div class="modelo-bg">
      <img src="~@/assets/img/modelo-cliente.png" alt />
    </div>
    <div class="tabs">
      <div class="tab has-text-weight-semibold" @click="cliente=true">Cliente</div>
      <div class="tab has-text-weight-semibold" @click="cliente=false">Consultor</div>
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
      cliente: true
    }
  }
}
</script>

<style>
</style>