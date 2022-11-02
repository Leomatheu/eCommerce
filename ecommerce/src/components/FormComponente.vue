<template>
    <div>   
        <form action="" @submit="EnviarFormulario($event)">
            <div>
                <input type="text" v-model="name">
            </div>
            <div>
                <input type="text" v-model="email">
            </div>
            <div>
                <input-submit/>
            </div>        
        </form>    
    </div>
</template>

<script>
    //imports dos componentes criados especificos
    import InputSubmit from './Formulario/InputSubmit.vue'
    //import InputText from './Formulario/InputText.vue'

    export default {
        name : 'FormComponente',

        components : {
            InputSubmit,
            //InputText
        },

        methods : {
            EnviarFormulario(e){
                e.preventDefault();

                const name = this.name;
                const email = this.email;

                console.log('Formulário enviado !!');
                console.log('O nome é: '+name);
                console.log('O email é: '+email);
            }
        },

        data () {
            return{
                name : "",
                email : ""
            }
        }
    }
</script>
