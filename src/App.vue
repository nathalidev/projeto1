<template>
    <div>
        <Header/>
        <PrimeiroComponente />
        <p class="paragrafo_pai">O dado do app é: {{ testando }}</p>
        <LifeCycle />
        <Pessoa />
    </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Header from './components/Header.vue'

    export default {
        name:"App",
        components: {
            PrimeiroComponente,
            LifeCycle,
            Pessoa, 
            Header
        },
        data() {
            return {
                testando: 'Teste'
            }
        }
    }
</script>

<style>
    body {
    background-color: #f5f7fa;
    color: #1e47a0;
    font-family: 'Segoe UI', sans-serif;
    margin: 10px;
    }

    a {
    color: #5c3d04;
    }

    .teste {
        background-color: #a1d1ff;
    }

    .paragrafo_pai{
        color: #5c3d04;
    }

</style>