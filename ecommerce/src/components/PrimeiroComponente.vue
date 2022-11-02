<template>
    <div>
        <h1 class="teste">Olá vue !</h1>
        <p>meu nome é: {{ nome }}</p>
        <MultiplosEventos/>
        <ReutilizacaoComponente/>
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
import ReutilizacaoComponente from './ReutilizacaoComponente.vue';

    
    export default {
        name: "PrimeiroComponente",

        data() {
            return {
                nome: "Leonardo"
            };
        },
        
        components: { MultiplosEventos, ReutilizacaoComponente }
    }

</script>
