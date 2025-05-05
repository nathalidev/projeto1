<template>
    <PrimeiroComponente />
    <p>O dado do app é: {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'

    export default {
        name:"App",
        components: {
            PrimeiroComponente,
            LifeCycle,
            Pessoa
        },
        data() {
            return {
                testando: 'Teste'
            }
        }
    }
</script>