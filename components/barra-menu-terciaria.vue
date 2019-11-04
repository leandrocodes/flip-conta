<template>
  <nav class="navbar is-terciaria is-transparent">
    <div class="navbar-brand">
      <nuxt-link to="/" class="navbar-item" href="#">
        <img src="~@/assets/img/flipconta-logo-white.png" alt="Flip Conta" width="112" height="28" />
      </nuxt-link>
      <div class="navbar-burger burger" data-target="navbarExampleTransparentExample">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>

    <div id="navbarHome" class="navbar-menu">
      <div class="navbar-end">
        <div class="navbar-item">
          <nuxt-link to="/login" class="button is-primary is-outlined is-rounded entrar">Logar na minha conta</nuxt-link>
        </div>
        <div class="navbar-item">
          <nuxt-link to="/consultor/cadastro" class="button is-light is-outlined is-rounded">Seja Consultor</nuxt-link>
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