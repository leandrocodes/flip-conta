<template>
  <nav class="navbar is-secondary is-transparent" id="nav2">
        <div class="navbar-brand">
          <nuxt-link to="/" class="navbar-item" href="#">
            <img src="~@/assets/img/flipconta-logo-purple.png" alt="Flip Conta" width="112" height="28" />
          </nuxt-link>
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
                <hr class="navbar-divider" />
                <a class="navbar-item has-text-dark" href>
                  <font-awesome-icon :icon="['fas', 'question-circle']" />Dúvidas
                </a>
                <hr class="navbar-divider" />
                <a class="navbar-item has-text-dark" href>
                  <span>
                    <font-awesome-icon :icon="['fas', 'clock']" />Horário de Funcionamento
                    <div class="horarios">
                      <p>
                      Segunda à Sexta <br />
                      8h30 às 19h30
                      </p>
                      <p>
                      Sábado <br />
                      9h30 às 19h30
                      </p>                      
                      <span>Exceto Domingos e Feriados</span>
                    </div>
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
                <nuxt-link to="/cliente/cadastro" class="button is-primary is-outlined is-rounded">Abrir minha conta grátis</nuxt-link>
            </div>
            <div class="navbar-item">
              <a href="#login" class="button is-primary is-outlined is-rounded">Logar na minha conta</a>
            </div>
            <div class="navbar-item">
              <a href="#consultor" class="button is-primary is-outlined is-rounded">Seja consultor</a>
            </div>
          </div>
        </div>
      </nav>
</template>

<script>
export default {

}
</script>

<style>

</style>