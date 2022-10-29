<template>
    <div>
        <p v-if="trabalhando" >Trabalho atualmente com as seguintes tecnologias: </p>
        <p v-else>Não possuo conhencimento nas seguintes tecnologias: </p>
        <ul>
            <li>Java</li>
            <li>Delphi</li>
            <li>VUE JS</li>
            <li>Test Complete</li>            
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
                endereco : "teste@teste.com.br",
                meulink : 'https://google.com',
                txtbtn : 'Mostrar e-mail'
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
        }
    }

</script>