<template>
    <section class="hero is-primary is-medium is-bold contact">
        <div class="hero-head">
            <barra-menu-secundaria></barra-menu-secundaria>
        </div>
        <div class="hero-body">
            <p class="subtitle">
            VOCÊ ESTÁ EM >> 
            <strong>CONTATO</strong>.
            </p>
        </div>
    </section>
    
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