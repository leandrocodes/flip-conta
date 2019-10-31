<template>
  <div class="artigo">
    <section class="hero is-bold">
      <div class="hero-head">
        <barra-menu-secundaria></barra-menu-secundaria>
      </div>
      <div class="hero-body">
        <!-- <p class="subtitle is-6 has-text-centered-mobile">
          você está em >>
          <strong>post</strong>
        </p> -->
        <div class="lead">
            <div class="columns">
              <div class="column">Charles Porto</div>
              <div class="column">15/06/2018</div>
              <div class="column">578</div>
            </div>
            <h1 class="title is-1 has-text-centered">O recurso de controle de contas a pagar do nosso Sistema ERP em Nuvem, centralizando</h1>
            <h2 class="subtitle is-2 has-text-centered">O recurso de controle de contas a pagar do nosso Sistema ERP em Nuvem, permite que você e sua equipe façam projeções de gastos e investimentos, centralizando informações sobre cliente, fornecedores, vencimentos e muito mais.</h2>
        </div>
      </div>
    </section>
    <div class="conteudo">
      <div class="columns is-centered is-mobile is-multiline">
        <div class="column post is-11-mobile is-12-tablet is-8-desktop">
            
        </div>
    </div>
    </div>
    
    <rodape></rodape>
  </div>
</template>

<script>

import BarraMenuSecundaria from '~/components/barra-menu-secundaria.vue'
import Rodape from '~/components/rodape.vue'

export default {
  components: {
    BarraMenuSecundaria,
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