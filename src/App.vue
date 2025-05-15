<template>
    <v-app id="inspire">  <!--tudo que eu fizer é dentro dele, corpo da aplicação-->
        
        <v-navigation-drawer :width="153" 
        v-model="drawer" app> <!--width larga da barra e o v-model drawer controla se a barra ta aberta ou fechada ligado a uma variavel -->
            <v-list-item title="Vue.js" subtitle="Lista de tarefas"></v-list-item> <!--Um item da lista dentro da barra lateral.
            Mostra título “Vue.js” e subtítulo “Lista de tarefas”.-->
            <v-divider></v-divider>

        <v-list dense>
            <!--items é um array que defini la embaixo/ to é pra onde a rota vai levar-->
            <v-list-item
            v-for="(item, index) in items" 
            :key="index"
            :to="item.to"
            link
        >
            <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>{{ item.title }}</v-list-item-title> <!--definindo os icones e titulos de cada item da lista-->
        </v-list-item>
        </v-list>
    </v-navigation-drawer>

    <v-app-bar
    >
        <template v-slot:image>
        <v-img
            gradient="to right, rgba(0, 0, 0, 1), rgba(50, 50, 50, 0.8)"
        ></v-img>
        </template>

        <template v-slot:prepend>
            <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        </template>

        <v-app-bar-title>Tarefex</v-app-bar-title>

        <v-btn icon>
            <v-icon>mdi-magnify</v-icon> <!--botões do lado direito da barra principal-->
        </v-btn>

        <v-btn icon>
            <v-icon>mdi-heart</v-icon>
        </v-btn>

        <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
    </v-app-bar>

    <v-main>
        <RouterView/>
    </v-main>
    </v-app>
</template>

<script setup>
    import { ref } from 'vue'

    const drawer = ref(null)
</script>

<script>
    export default {
    data: () => ({ drawer: null,
        items: [
            { title: "tarefas", icon: 'mdi-view-dashboard', to: '/tarefas'},
            { title: "sobre", icon: 'mdi-help-box', to: '/sobre'},
            ]
        }),
    }
</script>

<!--abaixo importo fonte do google e defino suas propriedades-->
<style> 
@import url('https://fonts.googleapis.com/css2?family=Bungee+Shade&family=Cal+Sans&family=Passion+One:wght@400;700;900&display=swap');
.v-app-bar-title {
    font-family: "Bungee Shade", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 2rem;
}
</style>