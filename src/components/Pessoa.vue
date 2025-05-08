<template>
    <div>
        <h2>Esta é a descrição de pessoa: {{ nome }}</h2>
        <Info :email="email" esta_trabalhando=false />
        <Formulario />
    </div>
</template>

<script>
import Info from './Info.vue'
import Formulario from './Formulario.vue' //importando os arquivos formulario e info que estão FORA da pasta form
    export default {
        name: "Pessoa",
        components: {
            Info,
            Formulario
        },
        data() {
            return {
                nome: "Nathã",
                email: 'nathalidorio@gmail.com'
            }
        }
    }
</script>