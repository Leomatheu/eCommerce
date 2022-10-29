<template>
    <img :src="avatar" :alt="descricao">
</template>

<script>
    export default {
        name : 'PictureComponente',

        data () {
            return {
                avatar : './IMG/icons8-usuário-100.png',
                descricao : 'imagem do avatar escolhido.'
            }
        }
    }
</script>