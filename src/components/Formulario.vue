<template>
    <form action="">
        <div>
            <InputText/>
        </div>
        <div>
            <Submit/> 
        </div>
    </form>
</template>

<script>
import InputText from './form/InputText.vue'  //importando o conteudo de input da pasta form
import Submit from './form/Submit.vue'
    export default {
        name: "Form",
        components: {
            InputText,
            Submit
        }
    }
</script>