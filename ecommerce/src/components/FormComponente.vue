<template>
    <div>
        <form action="">
            <div>
                <input-text/>
            </div>
            <div>
                <input-text/>
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
    import InputText from './Formulario/InputText.vue'

    export default {
        name : 'FormComponente',

        components : {
            InputSubmit,
            InputText
        }
    }
</script>
