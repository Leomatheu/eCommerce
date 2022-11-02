<template>
    <div>
        <p v-if="trabalhando" >Trabalho atualmente com as seguintes tecnologias: </p>
        <p v-else>Não possuo conhencimento nas seguintes tecnologias para back-end: </p>
        <ul>
            <li v-for="(tecnologias, index) in techs" v-bind:key="index">{{ tecnologias }}</li>         
        </ul>  
        <p>Utilizo as seguintes linguagens para front-end: </p>
        <ul>
            <li v-for="tecnologias in frontEnd" :key="tecnologias.id">{{ tecnologias.tipo }}</li>         
        </ul>  

        <div>
            <button @click="showMail()">{{txtbtn}}</button>
        </div>      

        <p v-show="email">Mande uma mensagem para: {{endereco}}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meulink">clique aqui </a></p>
        <div>
            <PictureComponente/>
        </div>
    </div>
</template>

<script>
    //import dos componentes 
    import PictureComponente from './PictureComponente.vue'

    export default {
        name : 'InfoComponente',

        data () {
            return {
                trabalhando : true,
                email : false,
                meulink : 'https://google.com',
                txtbtn : 'Mostrar e-mail',
                techs : ['Java', 'Delphi','VUE JS', 'Test Complete'],
                frontEnd : [
                    {id: 1 , tipo : 'HTML'},
                    {id: 2 , tipo : 'CSS'},
                    {id: 3 , tipo : 'JavaScript'}
                ]
            }
        },

        components : {
            PictureComponente
        },

        methods : {
            showMail() {
                this.email = !this.email
                if(!this.email){
                    this.txtbtn = 'Mostrar e-mail'
                }
                else {
                    this.txtbtn = 'Ocultar e-mail'
                }
            }
        },

        props : {
            endereco: String

            
        }
    }

</script>