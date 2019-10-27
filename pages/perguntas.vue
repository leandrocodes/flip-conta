<template>
  <div class="questions">
      <section class="hero is-primary is-bold">
      <div class="hero-head">
        <barra-menu-secundaria></barra-menu-secundaria>
      </div>
      <div class="hero-body">
        <p class="subtitle">
          VOCÊ ESTÁ EM >>
          <strong>PERGUNTAS</strong>
        </p>
      </div>
    </section>
    <div class="columns is-centered is-mobile">
      <div class="column is-10-mobile is-8-tablet is-4-desktop is-3-fullhd">
        <div class="texto-entrada has-text-centered">
          <h1 class="title has-text-primary has-text-weight-bold">Perguntas Frequentes</h1>
        </div>
        
        <div class="card">
            <header class="card-header">
                <p class="card-header-title">
                Como funciona a polica de ressarcimento?
                </p>
                <a href="#" class="card-header-icon" aria-label="Resposta">
                    <font-awesome-icon :icon="['fas', 'minus']" />
                </a>
            </header>
            <div class="card-content">
                <div class="content">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nulla impedit ducimus, odio quos eius excepturi enim itaque accusamus dolore nostrum eligendi velit veritatis iure sequi at, nesciunt repellendus soluta perspiciatis.
                </div>
            </div>
        </div>
        <hr class="card-divider"/>
        <div class="card">
            <header class="card-header">
                <p class="card-header-title">
                Quantos boletos posso efetuar mensalmente?
                </p>
                <a href="#" class="card-header-icon" aria-label="Resposta">
                    <font-awesome-icon :icon="['fas', 'plus']" />
                </a>
            </header>
        </div>    
        <hr class="card-divider"/>
        <div class="card">
            <header class="card-header">
                <p class="card-header-title">
                Como entrar em contato?
                </p>
                <a href="#" class="card-header-icon" aria-label="Resposta">
                    <font-awesome-icon :icon="['fas', 'plus']" />
                </a>
            </header>
        </div>
        <hr class="card-divider"/>
        <div class="card">
            <header class="card-header">
                <p class="card-header-title">
                Não consigo entrar na minha conta. E agora?
                </p>
                <a href="#" class="card-header-icon" aria-label="Resposta">
                    <font-awesome-icon :icon="['fas', 'plus']" />
                </a>
            </header>
        </div>  
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