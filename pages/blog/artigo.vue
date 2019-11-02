<template>
  <div class="artigo">
    <section class="hero is-bold is-large">
      <div class="hero-head">
        <barra-menu-secundaria></barra-menu-secundaria>
      </div>
      <div class="columns hero-body is-centered">
        <div class="column lead">
            <div class="columns info is-mobile is-centered">
              <div class="column esquerda is-4-mobile is-2-desktop has-text-right">
                <font-awesome-icon :icon="['fas', 'user-alt']" />
                <span class="is-size-7-mobile">Charles Porto</span>
              </div>
              <div class="column centro is-6-mobile is-3-desktop has-text-centered">
                <font-awesome-icon :icon="['fas', 'clock']" />
                <span class="is-size-7-mobile">15/06/2018 às 12h08</span>
              </div>
              <div class="column direita is-2-mobile is-2-desktop has-text-left">
                <font-awesome-icon :icon="['fas', 'eye']" />
                <span class="is-size-7-mobile">578</span>
              </div>
            </div>
            <div class="column has-text-centered">
              <h1 class="title is-size-2-desktop is-size-5-mobile has-text-centered">O recurso de controle de contas a pagar do nosso Sistema ERP em Nuvem</h1>
              <h2 class="subtitle is-size-5-desktop is-size-6-mobile has-text-centered has-text-white-ter">O recurso de controle de contas a pagar do nosso Sistema ERP em Nuvem, permite que você e sua equipe façam projeções de gastos e investimentos, centralizando informações sobre cliente, fornecedores, vencimentos e muito mais.</h2>
            </div>
        </div>
      </div>
    </section>

    <div class="columns article is-centered">
      <div class="column article_organizer">
        <div class="columns article_body is-centered is-mobile is-multiline">
          <div class="column has-text-justified is-11-mobile is-6-desktop">
            <figure class="image is-16by9 ">
              <img src="https://bulma.io/images/placeholders/640x360.png">
            </figure>
          </div>
          <div class="column has-text-justified is-11-mobile is-6-desktop">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Non repellendus natus molestias, consequuntur nesciunt suscipit dolorem optio quibusdam sit odit sapiente dicta esse, libero deleniti aliquam! Unde totam sequi earum?    
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. At quibusdam incidunt veniam, perspiciatis dolorem quisquam, quo, necessitatibus a minus amet dolore recusandae sequi doloribus consequatur qui. Est, totam. Quos, ullam?
            <br/>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem dignissimos accusamus repellendus suscipit nulla temporibus cumque. Id veniam nulla impedit in earum pariatur voluptate amet dolorem architecto, facere perferendis consequuntur.
            <br>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt facilis, possimus ipsam error nam debitis provident. Assumenda repellendus quasi, distinctio neque dolores, eligendi placeat sapiente harum expedita quisquam est reprehenderit?
          </div>
        </div>
        <div class="columns article_footer is-12 is-mobile is-multiline"> 
          <div class="column article_slider">
            <!-- TODO: 
            Slider
            -->
          </div>
          <div class="column article_references is-12">
            <span class="references_title subtitle is-size-6 has-text-weight-light">Fonte</span>
            <span class="references_link subtitle is-size-6 has-text-weight-light">Ministério da Economia</span>
          </div>
        </div>
        <div class="columns article_comments is-centered is-mobile is-multiline">
          <div class="column is-10 comments_fb has-background-white-ter has-text-centered">
            <p>Comentarios do Facebook</p>
          </div>
        </div>
      </div>  
    </div>
    
    <rodape></rodape>
  </div>
</template>

<script>

import BarraMenuSecundaria from '~/components/barra-menu-secundaria.vue'
import Rodape from '~/components/rodape.vue'

export default {
  components: {
    BarraMenuSecundaria,
    Rodape
  },
  data() {
    return {

    }
  }
}
</script>

<style>
</style>