<template>
  <div class="cadastro-fisica">
    <section class="hero is-bold">
      <div class="hero-head">
        <barra-menu-terciaria></barra-menu-terciaria>
      </div>
      <div class="hero-body">
        <p class="subtitle is-6 has-text-centered-mobile">
          você está em >>
          <strong>abrir minha conta grátis</strong>
          <!-- Colocar no media -->
        </p>
      </div>
    </section>]
    <div class="conteudo">
      <div v-if="fisica" class="columns is-centered is-mobile">
        <div class="column is-9-mobile is-6-tablet is-3-desktop is-3-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Pessoa Física</h4>
          </div>
          <form>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu nome completo" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu email" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Telefone" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Cidade" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Numero de notas emitidas mês?" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href class="button is-primary is-rounded">Cadastrar</a>
              </div>
            </div>
          </form>
        </div>
      </div>
      <div v-else class="columns is-centered is-mobile">
        <div class="column is-9-mobile is-6-tablet is-3-desktop is-3-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Pessoa Jurídica</h4>
          </div>
          <form>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu nome completo" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Insira seu email" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Telefone" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Cidade" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <input class="input is-primary is-rounded" type="text" placeholder="Numero de notas emitidas mês?" />
              </div>
            </div>
            <div class="field">
              <div class="control is-expanded">
                <a href class="button is-primary is-rounded">Cadastrar</a>
              </div>
            </div>
          </form>
        </div>
      </div>

      <div class="modelo-bg">
        <img src="~@/assets/img/modelo-cliente.png" alt />
      </div>
      <div class="tabs">
        <div class="tab has-text-weight-semibold" @click="fisica=true">Pessoa Física</div>
        <div class="tab has-text-weight-semibold" @click="fisica=false">Pessoa Jurídica</div>
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

    }
  }
}
</script>

<style>
</style>