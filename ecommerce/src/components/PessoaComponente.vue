<template>
    <div>
        <h2>Está é a descrição da pessoa: {{ nome }}</h2>
        <InfoComponente/>
        <div>
            <FormComponente/>
        </div>
    </div>
</template>

<script>
    //import dos componentes
    import InfoComponente from './InfoComponente.vue'
    import FormComponente from './FormComponente.vue'


    export default {
        name : 'PessoaComponente',

        data () {
            return {
                nome : "Pessoa XPTO"
            }
        },

        components : {
            InfoComponente,
            FormComponente
        }
    }
</script>
