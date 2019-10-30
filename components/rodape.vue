<template>
  <footer class="has-text-light">
    <div class="container">
      <div class="columns is-centered">
        <div class="column is-4 has-text-centered">
          <p>
            <font-awesome-icon :icon="['fas', 'headset']" />| 123 456 789
          </p>
        </div>
        <div class="column is-4 has-text-centered">
          <p>
            <font-awesome-icon :icon="['fas', 'envelope']" />| contato@flipconta.com.br
          </p>
        </div>
        <div class="column is-4 has-text-centered">
          <p>
            <font-awesome-icon :icon="['fas', 'map-marker-alt']" />| raja, 123 - belo horizonte
          </p>
        </div>
      </div>
      <div class="columns is-centered is-multiline is-mobile">
        <div class="column is-2-desktop is-12-mobile has-text-centered-mobile">
          <h3 class="is-uppercase has-text-left has-text-centered-mobile">nossos serviços</h3>
          <div class="text" style="margin-top: 15px;">
            <a class="has-text-light" href>boletos</a>
            <br />
            <a class="has-text-light" href>notas fiscais</a>
            <br />
            <a class="has-text-light" href>data programada</a>
            <br />
            <a class="has-text-light" href>boletos</a>
            <br />
            <a class="has-text-light" href>notas fiscais</a>
            <br />
            <a class="has-text-light" href>data programada</a>
          </div>
        </div>
        <div class="column is-4-desktop is-offset-2-desktop is-12-mobile has-text-centered-mobile">
          <h3 class="is-uppercase has-text-left has-text-centered-mobile">sobre nós</h3>
          <div class="text" style="margin-top: 15px;">
            <a class="has-text-light" href>flipconta</a>
            <br />
            <a class="has-text-light" href>termos de uso</a>
            <br />
            <a class="has-text-light" href>politicas de privacidade</a>
            <br />
            <a class="has-text-light" href>blog</a>
            <br />
            <a class="has-text-light" href>berguntas frequentes</a>
            <br />
            <a class="has-text-light" href>contato</a>
          </div>
        </div>
        <div class="column is-2-desktop is-12-mobile has-text-centered-mobile">
          <h3 class="is-uppercase has-text-left has-text-centered-mobile">baixe o flipconta</h3>
          <div class="text" style="margin-top: 15px;">
            <img src="~@/assets/img/selo-google.png" alt="">
            <img src="~@/assets/img/selo-apple.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style>
</style>