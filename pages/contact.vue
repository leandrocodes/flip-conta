<template>
    <div>
        <section class="hero is-primary is-bold contact">
            <div class="hero-head">
                <barra-menu-secundaria></barra-menu-secundaria>
            </div>
            <div class="hero-body">
                <p class="subtitle">
                VOCÊ ESTÁ EM >> 
                <strong>CONTATO</strong>
                </p>
            </div>
        </section>
        <form>
            <div class="texto-entrada has-text-centered">
                <h1 class="title has-text-link">Fale Conosco</h1>
                <h3 class="subtitle has-text-link">
                Tire dúvidas, elogios e mais
                </h3>
            </div>
            <div class="field is-grouped is-grouped-centered">
                <div class="control">
                    <input class="input" type="text" placeholder="Nome">
                </div>
                <div class="control">
                    <input class="input" type="text" placeholder="Email">
                </div>
            </div>
            <div class="field is-grouped is-grouped-centered">
                <div class="control">
                    <input class="input" type="text" placeholder="Celular">
                </div>
                <div class="control">
                    <input class="input" type="text" placeholder="Assunto">
                </div>
            </div>
            <div class="field">
                <div class="control">
                    <textarea class="textarea" placeholder="e.g. Hello world">Sua Mensagem</textarea>
                </div>
            </div>
            <div class="field">
                <div class="control">
                    <a href class="button is-link is-rounded">Enviar Mensagem</a>
                </div>
            </div>
        </form>
    </div>    
    </template>

<script>

import BarraMenuSecundaria from '~/components/barra-menu-secundaria.vue'

export default {
    components: {
        BarraMenuSecundaria
    },
    data() {
        return{

        }
    }
}
</script>

<style>

</style>