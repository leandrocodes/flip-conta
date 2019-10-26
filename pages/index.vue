<template>
<section class="hero is-primary is-medium">
  <!-- Hero head: will stick at the top -->
  <div class="hero-head">
    <nav class="navbar is-primary is-transparent">
      <div class="navbar-brand">
        <a class="navbar-item" href="#">
          <img src="~@/assets/img/flipconta-logo-white.png" alt="Flip Conta" width="112" height="28">
        </a>
        <div class="navbar-burger burger" data-target="navbarExampleTransparentExample">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>

      <div id="navbarHome" class="navbar-menu">
        <div class="navbar-end">
          <div class="navbar-item">
            <a href="" class="button is-link is-outlined is-rounded">início</a>
          </div>
          <div class="navbar-item">
            <a href="" class="button is-link is-outlined is-rounded">soluções</a>
          </div>
          <div class="navbar-item">
            <a href="" class="button is-link is-outlined is-rounded">preços</a>
          </div>
          <div class="navbar-item has-dropdown is-hoverable">
            <div class="navbar-link is-arrowless is-rounded">
              <a href="" class="button is-link is-outlined is-rounded">suporte</a>
            </div>
            <div class="navbar-dropdown is-boxed">
              <a class="navbar-item has-text-dark" href="">
                Chat
              </a>
              <hr class="navbar-divider">
              <a class="navbar-item has-text-dark" href="">
                Fone
              </a>
              <hr class="navbar-divider">
              <a class="navbar-item has-text-dark" href="">
                contato@flipconta.com
              </a>
              <hr class="navbar-divider">
              <a class="navbar-item has-text-dark" href="">
                <span>
                  Horário de Funcionamento<br><br>
                  <span>
                    Segunda à Sexta<br>
                    8h30 às 19h30<br><br>
                    Sábado<br>
                    9h30 às 19h30<br><br>
                    <span>
                      Exceto Domingos e Feriados
                    </span>
                  </span>
                </span>    
              </a>
            </div>
          </div>
          <div class="navbar-item">
            <a href="#facebook" class="button is-rounded is-link is-outlined social">
              <font-awesome-icon :icon="['fab', 'facebook-f']"/>
            </a>
          </div>
          <div class="navbar-item">
            <a href="#twitter" class="button is-rounded is-link is-outlined social">
              <font-awesome-icon :icon="['fab', 'twitter']"/>
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
    <p class="title">
      Documentation
    </p>
    <p class="subtitle">
      Everything you need to <strong>create a website</strong> with Bulma
    </p>
  </div>

</section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
  .navbar-dropdown .navbar-item:hover{
    color:purple!important;
  }
  .social{
    width: 2.25em;
    height: 2.25em;
  }

</style>
