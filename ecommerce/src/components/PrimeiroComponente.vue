<template>
    <div>
        <h1 class="teste">Olá vue !</h1>
        <p>meu nome é: {{ nome }}</p>
    </div>
</template>

<script>
    
    export default {
        name : "PrimeiroComponente",

        data () {
            return{
                nome : "Leonardo"
            }
        }
        
    }

</script>