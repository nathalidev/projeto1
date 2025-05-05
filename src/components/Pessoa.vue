<template>
    <h2>Esta é a descrição de pessoa: {{ nome }}</h2>
</template>

<script>
    export default {
        name: "Pessoa",
        data() {
            return {
                nome: "Nathã"
            }
        }
    }
</script>