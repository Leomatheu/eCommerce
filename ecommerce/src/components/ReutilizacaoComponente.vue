<template>
    <div>
        <button @click="ativa()">Reutilizado</button>

        <span v-show="ativou">Ativado !</span>
    </div>
</template>

<script>
    export default {
        name : 'ReutilizacaoComponente',

        methods : {
            ativa(){
                this.ativou = !this.ativou;
            }
        },

        data () {
            return {
                ativou : false
            }
        }
    }
</script>