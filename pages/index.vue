<template>
  <div class="container">
<nav class="navbar is-link">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <img src="~@/assets/img/flipconta-logo-white.png" alt="Bulma: a modern CSS framework based on Flexbox" width="112" height="28">
    </a>
    <div class="navbar-burger burger" data-target="navbarExampleTransparentExample">
      <span></span>
      <span></span>
      <span></span>
    </div>
  </div>

  <div id="navbarHome" class="navbar-menu">
    <div class="navbar-end">
      <a href="#incio" class="navbar-item">
        início
      </a>
      <a href="#solucoes" class="navbar-item">
        soluções
      </a>
      <a href="#preco" class="navbar-item">
        preço
      </a>
      <div class="navbar-item has-dropdown is-hoverable">
        <a class="navbar-link is-arrowless" href="https://bulma.io/documentation/overview/start/">
          suporte
        </a>
        <div class="navbar-dropdown is-boxed">
          <a class="navbar-item" href="https://bulma.io/documentation/overview/start/">
            Overview
          </a>
          <a class="navbar-item" href="https://bulma.io/documentation/modifiers/syntax/">
            Modifiers
          </a>
          <a class="navbar-item" href="https://bulma.io/documentation/columns/basics/">
            Columns
          </a>
          <a class="navbar-item" href="https://bulma.io/documentation/layout/container/">
            Layout
          </a>
          <a class="navbar-item" href="https://bulma.io/documentation/form/general/">
            Form
          </a>
          <hr class="navbar-divider">
          <a class="navbar-item" href="https://bulma.io/documentation/elements/box/">
            Elements
          </a>
          <a class="navbar-item is-active" href="https://bulma.io/documentation/components/breadcrumb/">
            Components
          </a>
        </div>
      </div>
      <a href="#facebook" class="navbar-item">
        F
      </a>
      <a href="#twiter" class="navbar-item">
        T
      </a>
      <a href="#abrir-conta" class="navbar-item">
        Abrir minha conta grátis
      </a>
      <a href="#login" class="navbar-item">
        Logar na minha conta
      </a>
      <a href="#consultor" class="navbar-item">
        Seja consultor
      </a>
    </div>
  </div>
</nav>

<section class="hero is-link">
  <div class="hero-body">
    <p class="title">
      Documentation
    </p>
    <p class="subtitle">
      Everything you need to <strong>create a website</strong> with Bulma
    </p>
  </div>
</section>
</div>
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
</style>
