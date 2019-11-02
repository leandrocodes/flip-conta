<template>
  <div class="indicacao">
    <section class="hero indication">
      <div class="hero-head">
        <barra-menu-terciaria></barra-menu-terciaria>
      </div>
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-offset-2 is-5 has-text-left">
              <p class="has-text-light">código do convite</p>
              <a class="button is-light has-text-weight-bold">CHARLES101</a>
              <p class="is-size-4 has-text-white has-text-weight-bold">
                <span>Charles</span> convidou você
                <br />para conhecer a flipconta.
              </p>
              <p class="is-size-4 has-text-white has-text-weight-bold">uma simplicidade na sua gestão.</p>
              <a class="button is-primary has-text-white has-text-weight-semibold">cadastrar</a>
            </div>
          </div>
        </div>
      </div>
      <div class="modelo-convite">
        <img src="~@/assets/img/modelo_convite.png" alt srcset />
      </div>
    </section>

    <div class="container cadastro">
      <div class="columns is-multiline is-mobile">
        <div class="column is-12-desktop is-12-full-hd is-12-widescreen is-12-mobile is-12-tablet has-text-grey-dark">
          <p>Cadastre-se agora.</p>
        </div>
        <div class="column is-12-desktop is-12-full-hd is-12-widescreen is-12-mobile is-12-tablet has-text-grey-dark">
          <ol>
            <li>Entre no site e baixe o app;</li>
            <li>Escolha a opção TENHO UM CONVITE;</li>
            <li>Use o código CHARLES101;</li>
            <li>Faça o cadastro;</li>
            <li>Pronto! Você e a pessoa que te indicou ganha dinheiro! ;)</li>
          </ol>
        </div>
        <div class="column is-12-desktop is-12-full-hd is-12-widescreen is-12-mobile is-12-tablet has-text-grey-dark">
          <p>É melhor correr! Esse código so pode ser usado por 1 pessoa.</p>
        </div>
        <div class="column is-12-desktop is-12-full-hd is-12-widescreen is-12-mobile is-12-tablet indication-pic">
          <img src="~@/assets/img/indicacao.png" alt srcset />
          <div class="card-txt1">
            <h4 class="has-text-weight-bold is-size-4 is-uppercase">agora é só sombra e água fresca!!!</h4>
            <p>
              Agora é descansar
              <br />e esperar a minha conta engordar!!! 😏🤑
            </p>
          </div>
          <div class="card-txt2">
            <h4 class="has-text-weight-bold is-size-4 is-uppercase">Vida boa é assim!!!</h4>
            <p>
              Agora é deixa que a Flipconta
              <br />trabalhe por mim... 😏🤑
            </p>
          </div>
        </div>
      </div>
    </div>
    <rodape></rodape>
  </div>
</template>

<script>
import barraMenuTerciaria from '../components/barra-menu-terciaria.vue'
import rodape from '../components/rodape'
export default {
  components: {
    barraMenuTerciaria,
    rodape
  }
}
</script>

<style>
</style>