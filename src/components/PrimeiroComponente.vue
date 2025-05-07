<template>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }} tenho {{ idade }} e  trabalho como {{ profissao }}</p>
    <MultiplosEventos />
    <Reutilizacao />
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
import Reutilizacao from './Reutilizacao.vue';
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data() {
            return {
                nome: 'Nathã',
                idade: 20,
                profissao: 'Programador',
            }
        }
    }
</script>