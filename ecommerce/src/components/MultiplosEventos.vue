<template>
    <div>
        <button @click="Primeiro($event), Segundo($event), terceiro()">Ativar Multiplos Eventos</button>
        <p> {{ multiplosEventos }} </p>
    </div>
</template>


<script>
    export default {
        name : 'MultiplosEventos',

        data () {
            return {
                multiplosEventos : ""
            }
        },

        methods : {
            Primeiro(e){
                e.preventDefault();
                this.multiplosEventos = "Primeiro evento ativado !"
            },

            Segundo(e){
                e.preventDefault();
                setTimeout(() => this.multiplosEventos = "Segundo evento ativado !", 500);
            },

            terceiro(){
                setTimeout(() => this.multiplosEventos = "", 2000);
            }
        }

    }


</script>

<style  scoped>
    div {
        margin: 100px;
    }
</style>