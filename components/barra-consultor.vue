<template>
  <nav class="navbar is-primary is-transparent is-fixed-top" id="nav">
    <div class="navbar-brand" style="background: none;">
      <nuxt-link to="/" class="navbar-item" href="#">
        <img id="nav-logo" src="~@/assets/img/flipconta-logo-purple.png" alt="Flip Conta" width="112" height="28" />
      </nuxt-link>
      <div class="navbar-burger burger has-text-dark"  @click="showNav = !showNav" :class="{ 'is-active': showNav }">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>

    <div id="navbarHome" class="navbar-menu" :class="{ 'is-active': showNav }">
      <div class="navbar-end">
        <div class="navbar-item">
          <nuxt-link to="/consultor" class="button is-outlined is-rounded">
            <p>Início <font-awesome-icon :icon="['fas', 'home']" /> </p>
          </nuxt-link>
        </div>
        <div class="navbar-item">
          <nuxt-link to="/login" class="button is-outlined is-rounded">
            <p>Minha conta <font-awesome-icon :icon="['fas', 'user']" /></p>
          </nuxt-link>
        </div>
        <div class="navbar-item">
          <nuxt-link to="/consultor/cadastro" class="button is-outlined is-rounded">
            <p>Cadastre-se <font-awesome-icon :icon="['fas', 'comments']" /> </p>
          </nuxt-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showNav: false
    }
  }
}
</script>

<style>
.navbar {
  transition: all 0.3s ease-in-out;
}
</style>