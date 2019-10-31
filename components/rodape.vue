<template>
  <!-- TODO: 
          font size responsivo
  -->
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
            <img src="~@/assets/img/selo-google.png" alt />
            <img src="~@/assets/img/selo-apple.png" alt />
          </div>
        </div>
      </div>
      <div class="columns is-mobile is-multiline is-centered" style="margin-bottom: 100px">
        <div class="column is-2-desktop is-12-mobile is-offset-1-desktop has-text-centered-mobile">
          <img src="~@/assets/img/flipconta-logo-white.png" alt="">
        </div>
        <div class="column is-5 is-offset-1 has-text-left has-text-centered-mobile">
          <p>somos uma startup que trouxe inovação na forma do seu financeiro trabalhar. ganhe tempo e agilidade no seu fluxo de cobrança regular.</p>
        </div>
        <div class="column is-2-desktop is-12-mobile is-offset-1-desktop has-text-centered">
          <h4 class="is-size-5 has-text-weight-semibold has-text-centered">SIGA-NOS</h4>
          <div class="social-links" style="margin-top: 10px;">

            <a href="#facebook" class="fb-link button is-rounded is-light is-outlined social">
              <font-awesome-icon class="is-size-3" :icon="['fab', 'facebook-f']" />
            </a>
            <a href="#instagram" class="insta-link button is-rounded is-light is-outlined social">
              <font-awesome-icon class="is-size-3" :icon="['fab', 'instagram']" />
            </a>
            <a href="#twitter" class="twt-link button is-rounded is-light is-outlined social">
              <font-awesome-icon class="is-size-3" :icon="['fab', 'twitter']" />
            </a>
            <a href="#youtube" class="yt-link button is-rounded is-light is-outlined social">
              <font-awesome-icon class="is-size-3" :icon="['fab', 'youtube']" />
            </a>
          </div>
        </div>
      </div>
      <div class="direitos columns is-mobile is-centered is-multiline">
        <div class="column is-4-desktop is-8-mobile">
          <p class="has-text-light">2019. Todos os direitos reservados.</p>
        </div>
        <div class="column is-4-desktop is-offset-4-desktop is-2-mobile has-text-centered">
          <img src="~@/assets/img/logo-vmais.png" alt="">
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