<template>
  <div class="artigo">
    <section class="hero is-bold is-large">
      <div class="hero-head">
        <barra-menu-secundaria></barra-menu-secundaria>
      </div>
      <div class="columns hero-body">
        <div class="column lead">
            <div class="columns info is-centered is-mobile">
              <div class="column is-4-mobile is-1-desktop has-text-centered"><span class="is-size-7-mobile">Charles Porto</span></div>
              <div class="column is-4-mobile is-1-desktop has-text-centered"><span class="is-size-7-mobile">15/06/2018</span></div>
              <div class="column is-4-mobile is-1-desktop has-text-centered"><span class="is-size-7-mobile">578</span></div>
            </div>
            <h1 class="title is-size-2-desktop is-size-5-mobile has-text-centered">O recurso de controle de contas a pagar do nosso Sistema ERP em Nuvem, centralizando</h1>
            <h2 class="subtitle is-size-4-desktop is-size-6-mobile has-text-centered has-text-white-ter">O recurso de controle de contas a pagar do nosso Sistema ERP em Nuvem, permite que você e sua equipe façam projeções de gastos e investimentos, centralizando informações sobre cliente, fornecedores, vencimentos e muito mais.</h2>
        </div>
        <!-- <p class="subtitle is-6 has-text-centered-mobile">
          você está em >>
          <strong>post</strong>
        </p> -->
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