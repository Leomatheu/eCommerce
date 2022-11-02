<template>
    <div>
        <h2>Está é a descrição da pessoa: {{ nome }}</h2>
        <InfoComponente :endereco= "endereco"/>
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
                nome : "Pessoa XPTO",
                endereco : "email.com.beerre"
            }
        },

        components : {
            InfoComponente,
            FormComponente
        }
    }
</script>
