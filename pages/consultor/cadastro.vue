<template>
  <div class="anunciante">
    <section class="hero is-bold">
      <div class="hero-head">
        <barra-menu-terciaria></barra-menu-terciaria>
      </div>
      <div class="hero-body">
        <p class="subtitle is-6 has-text-centered-mobile">
          você está em >>
          <strong>cadastro do consultor</strong>
          <!-- Colocar no media -->
        </p>
      </div>
    </section>
    <div class="conteudo">
      <div class="columns is-centered is-mobile">
        <div class="column is-10-mobile is-8-tablet is-5-desktop is-3-fullhd">
          <div class="texto-inicio has-text-centered">
            <h4 class="subtitle is-black has-text-weight-bold">Insire seus dados para o cadastro</h4>
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
              <div class="control is-expanded" style="display: flex; align-items: center; justify-content: center;">
                <input type="checkbox" />
                <div style="margin-left: 1em;">
                  Eu concodo com os
                  <a href="#" class="has-text-primary">termos e dondições</a> de uso
                </div>
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
      <img class="modelo-consultor" src="~@/assets/img/modelo-consultor.png" alt srcset />
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