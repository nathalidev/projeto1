<template>
    <div>
        <p v-if ="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em buscar de novas oportunidades.</p>
        <p>Utilizo as seguintes tecnologias</p>
        <ul>
            <li>Javascript</li>
            <li>PHP</li>
            <li>Python</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show = "mostrar_email && !esta_trabalhando">Mande uma mensagem para {{ email }}</p>
        <p class ="teste">Para acessar meu portifólio <a v-bind:href ="meu_link" target = "blank">Basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<!--use o v-show se o "senão não existir"-->
<!--exemplo quero mostrar algo se a variavel exemplo for verdadeira mais e se ela não for? ai não faço nada nesse caso e ai que entrar o v-show se não usar v-if etc...-->

<script>
import Picture from './Picture.vue'
    export default {
        name: "Info",
        components: {
            Picture
        },
        data() {
            return {
                esta_trabalhando: false,
                mostrar_email:false,
                email: "nathalidorio@gmail.com",
                meu_link: "https://www.inter.it/it",
                textoBotao: "Mostrar email"
            };
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this. mostrar_email;
                if(!this.mostrar_email){
                    this.textoBotao = "Mostrar email";
                }else{
                    this.textoBotao = "Esconder email";
                }
            }
        }
    }
</script>