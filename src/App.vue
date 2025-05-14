<template>
    <v-app id="inspire">
        
        <v-navigation-drawer :width="153"
        v-model="drawer" app>
            <v-list-item title="Vue.js" subtitle="Lista de tarefas"></v-list-item>
            <v-divider></v-divider>

        <v-list dense>
            <v-list-item
            v-for="(item, index) in items"
            :key="index"
            link
        >
            <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
        </v-list>
    </v-navigation-drawer>
    <v-app-bar :elevation="5" color="#311B92" app fixed class="border-double">
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

        <v-app-bar-title>Nathã Lidório</v-app-bar-title>
    </v-app-bar>

    <v-main>
        <!--  -->
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
            { title: "Tarefas", icon: 'mdi-view-dashboard'},
            { title: "Sobre", icon: 'mdi-help-box'},
            ]
        }),
    }
</script>

<style>
.border-double {
  border: 3px double #5E35B1; /* Borda dupla, aplicada diretamente aqui no estilo */
}
</style>