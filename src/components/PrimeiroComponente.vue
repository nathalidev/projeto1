<template>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }} tenho {{ idade }} e  trabalho como {{ profissao }}</p>
</template>

<script>
    export default {
        name: 'PrimeiroComponente',
        data() {
            return {
                nome: 'Nathã',
                idade: 20,
                profissao: 'Programador',
            }
        }
    }
</script>