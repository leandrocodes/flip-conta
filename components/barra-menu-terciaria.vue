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
          <a href="#login" class="button entrar is-rounded">Logar na minha conta</a>
        </div>
        <div class="navbar-item">
          <a href="#consultor" class="button is-white is-outlined is-rounded">Seja consultor</a>
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