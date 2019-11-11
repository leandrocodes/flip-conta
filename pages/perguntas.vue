<template>
  <div class="questions">
    <section class="hero">
      <div class="hero-head">
        <barra-menu-secundaria></barra-menu-secundaria>
      </div>
      <div class="hero-body">
        <p class="subtitle is-6">
          VOCÊ ESTÁ EM >>
          <strong>PERGUNTAS</strong>
        </p>
      </div>
    </section>
    <div class="conteudo">
      <div class="columns is-centered is-mobile">
        <div class="column is-10-mobile is-8-tablet is-4-desktop is-3-fullhd">
          <div class="texto-inicio has-text-centered">
            <h1 class="title has-text-primary has-text-weight-bold">Perguntas Frequentes</h1>
          </div>
          <div class="contents">
            <h5 class="subtitle is-5 has-text-black has-text-weight-bold">License</h5>
            <div class="card">
              <header class="card-header">
                <p class="card-header-title has-text-primary">Como funciona a polica de ressarcimento?</p>
                <a @click="resposta1 = !resposta1" class="card-header-icon has-text-primary" aria-label="Resposta">
                  <font-awesome-icon v-if="resposta1 === true" :icon="['fas', 'minus']" />
                  <font-awesome-icon v-else :icon="['fas', 'plus']" />
                </a>
              </header>
              <div class="card-content">
                <div
                  v-if="resposta1 === true"
                  class="content has-text-justified"
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nulla impedit ducimus, odio quos eius excepturi enim itaque accusamus dolore nostrum eligendi velit veritatis iure sequi at, nesciunt repellendus soluta perspiciatis.</div>
              </div>
            </div>
            <hr class="card-divider" />
            <div class="card">
              <header class="card-header">
                <p class="card-header-title has-text-primary">Quantos boletos posso efetuar mensalmente?</p>
                <a @click="resposta2 = !resposta2" class="card-header-icon has-text-primary" aria-label="Resposta">
                  <font-awesome-icon v-if="resposta2 === true" :icon="['fas', 'minus']" />
                  <font-awesome-icon v-else :icon="['fas', 'plus']" />
                </a>
              </header>
              <div class="card-content">
                <div
                  v-if="resposta2 === true"
                  class="content has-text-justified"
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nulla impedit ducimus, odio quos eius excepturi enim itaque accusamus dolore nostrum eligendi velit veritatis iure sequi at, nesciunt repellendus soluta perspiciatis.</div>
              </div>
            </div>
            <hr class="card-divider" />
            <div class="card">
              <header class="card-header">
                <p class="card-header-title has-text-primary">Como entrar em contato?</p>
                <a @click="resposta3 = !resposta3" class="card-header-icon has-text-primary" aria-label="Resposta">
                  <font-awesome-icon v-if="resposta3 === true" :icon="['fas', 'minus']" />
                  <font-awesome-icon v-else :icon="['fas', 'plus']" />
                </a>
              </header>
              <div class="card-content">
                <div
                  v-if="resposta3 === true"
                  class="content has-text-justified"
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nulla impedit ducimus, odio quos eius excepturi enim itaque accusamus dolore nostrum eligendi velit veritatis iure sequi at, nesciunt repellendus soluta perspiciatis.</div>
              </div>
            </div>
            <hr class="card-divider" />
            <div class="card">
              <header class="card-header">
                <p class="card-header-title has-text-primary">Não consigo entrar em minha conta. E agora?</p>
                <a @click="resposta4 = !resposta4" class="card-header-icon has-text-primary" aria-label="Resposta">
                  <font-awesome-icon v-if="resposta4 === true" :icon="['fas', 'minus']" />
                  <font-awesome-icon v-else :icon="['fas', 'plus']" />
                </a>
              </header>
              <div class="card-content">
                <div
                  v-if="resposta4 === true"
                  class="content has-text-justified"
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nulla impedit ducimus, odio quos eius excepturi enim itaque accusamus dolore nostrum eligendi velit veritatis iure sequi at, nesciunt repellendus soluta perspiciatis.</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="questions-img">
      <img src="~@/assets/img/perguntas.png" alt srcset />
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
      resposta1: false, resposta2: false, resposta3: false, resposta4: false
    }
  }
}
</script>

<style>
</style>