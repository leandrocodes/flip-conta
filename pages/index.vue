<template>
  <section class="hero is-primary is-large home">
    <!-- Hero head: will stick at the top -->
    <div class="hero-head">
      <nav class="navbar is-primary is-transparent">
        <div class="navbar-brand">
          <a class="navbar-item" href="#">
            <img src="~@/assets/img/flipconta-logo-white.png" alt="Flip Conta" width="112" height="28" />
          </a>
          <div class="navbar-burger burger" data-target="navbarExampleTransparentExample">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>

        <div id="navbarHome" class="navbar-menu">
          <div class="navbar-end">
            <div class="nav-link navbar-item">
              <a href class="button is-light is-outlined is-rounded">início</a>
            </div>
            <div class="nav-link navbar-item">
              <a href class="button is-light is-outlined is-rounded">soluções</a>
            </div>
            <div class="nav-link navbar-item">
              <a href class="button is-light is-outlined is-rounded">preços</a>
            </div>
            <div class="nav-link navbar-item has-dropdown is-hoverable">
              <div class="navbar-link is-arrowless is-rounded">
                <a href class="button is-light is-outlined is-rounded">suporte</a>
              </div>
              <div class="navbar-dropdown is-boxed">
                <a class="navbar-item has-text-dark" href>
                  <font-awesome-icon :icon="['fas', 'comment-alt']" />Chat
                </a>
                <hr class="navbar-divider" />
                <a class="navbar-item has-text-dark" href>
                  <font-awesome-icon :icon="['fas', 'phone-volume']" />Fone
                </a>
                <hr class="navbar-divider" />
                <a class="navbar-item has-text-dark" href>
                  <font-awesome-icon :icon="['fas', 'envelope']" />contato@flipconta.com
                </a>
                <a class="navbar-item has-text-dark" href>
                  <font-awesome-icon :icon="['fas', 'question-circle']" />Dúvidas
                </a>
                <hr class="navbar-divider" />
                <a class="navbar-item has-text-dark" href>
                  <font-awesome-icon :icon="['fas', 'clock']" />
                  <span>
                    Horário de Funcionamento
                    <br />
                    <br />
                    <span>
                      Segunda à Sexta
                      <br />8h30 às 19h30
                      <br />
                      <br />Sábado
                      <br />9h30 às 19h30
                      <br />
                      <br />
                      <span>Exceto Domingos e Feriados</span>
                    </span>
                  </span>
                </a>
              </div>
            </div>
            <div class="navbar-item">
              <a href="#facebook" class="fb-link button is-rounded is-light is-outlined social">
                <font-awesome-icon :icon="['fab', 'facebook-f']" />
              </a>
            </div>
            <div class="navbar-item">
              <a href="#twitter" class="twt-link button is-rounded is-light is-outlined social">
                <font-awesome-icon :icon="['fab', 'twitter']" />
              </a>
            </div>
            <div class="navbar-item">
              <a href="#abrir-conta" class="button is-link is-outlined is-rounded">Abrir minha conta grátis</a>
            </div>
            <div class="navbar-item">
              <a href="#login" class="button is-link is-outlined is-rounded">Logar na minha conta</a>
            </div>
            <div class="navbar-item">
              <a href="#consultor" class="button is-link is-outlined is-rounded">Seja consultor</a>
            </div>
          </div>
        </div>
      </nav>
    </div>

    <div class="hero-body">
      <p class="title">FLIPCONTA</p>
      <p class="subtitle">
        Lorem ipsum dolor
        <strong>sit amet</strong>.
      </p>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data() {
    return {

    }
  },
  methods: {
    mouseInHover(event) {
      event.target.classList.remove('is-light')
      event.target.classList.add('is-primary')
    },
    mouseOutHover(event) {
      event.target.classList.remove('is-primary')
      event.target.classList.add('is-light')
    }
  }
}
</script>

<style>
</style>
