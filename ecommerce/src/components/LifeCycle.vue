<template>
   <div>
        <h1>Meu nome é: {{ nome }}</h1>

   </div> 
</template>

<script>
    export default {
        name : "LifeCycle",

        data(){
            return{
                nome : 'ainda não sei'
            }
        },

        created(){
            setTimeout(() => {
                this.nome = "Leonardo Matheus."
            }, 2000)

            this.LifeCycle();
            
        },

        mounted (){
            setTimeout(() => {
                this.nome = "de Freitas Roa."
            }, 3000)
            
        },

        methods : {
            LifeCycle(){
                console.log("Executou o método");
            }
        }
    }
</script>