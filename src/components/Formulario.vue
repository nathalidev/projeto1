<template>
    <div>
        <h1>Formulário</h1>
        <form action="" @submit="enviarFormulario">
            <div>
                <input type="text" v-model="name">
            </div>
            <div>
                <input type="text" v-model="email">
            </div>
            <div>
                <Submit/> 
            </div>
        </form>
        <p>Conteúdo</p>
        <p>Conteúdo</p>
        <p>Conteúdo</p>
    </div>
</template>

<script>
import InputText from './form/InputText.vue'  //importando o conteudo de input da pasta form
import Submit from './form/Submit.vue'
    export default {
        name: "Form",
        components: {
            InputText,
            Submit
        },
        data(){
            return {
                name: "",
                email: "",
            }
        },
        methods: {
            enviarFormulario(e) {
                e.preventDefault(); // impede o comportamento padrão do formulário
                const name = this.name;
                const email = this.email;
                console.log("Nome: "+ name);
                console.log("Email: "+ email);
            }
        }
    }
</script>

<style scoped>
    p{
        margin: 50px;
    }

</style>