<template>
    <img :src="avatar" :alt="descricao">
    <EmitComponente @mudar-imagem="mudarImagem()"/>
</template>

<script>
    import EmitComponente from './EmitComponente.vue';

    export default {
        name : 'PictureComponente',

        data () {
            return {
                avatar : './IMG/icons8-usuário-100.png',
                descricao : 'imagem do avatar escolhido.'
            }
        },

        components : {
            EmitComponente
        },

        methods : {
            mudarImagem(){
                this.avatar = './IMG/icons8-dever-de-casa-80.png';
            }
        }
    }
</script>