<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default{
    name: 'LifeCycle',
    data () {
        return {
            nome: 'Ainda não sei'
        }
    },
    created() {
        setTimeout(() => {
            this.nome = 'Nathã'
        }, 2000)
    },
    mounted() {
        setTimeout(() => {
            this.nome = 'Lidório'
        }, 4000)
    },
}
</script>
