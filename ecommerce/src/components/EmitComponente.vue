<template>
    <div>
        <button @click="$emit('mudarImagem')">Mudar imagem do avatar</button>
    </div>
</template>

<script>
    export default {
        name : "EmitComponente",

        emits :['mudarImagem']
    }

</script>