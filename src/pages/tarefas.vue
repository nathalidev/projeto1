<!-- src/pages/tarefas.vue -->
<template>
    <div>
         <v-list lines="three">
      <v-list-subheader>User Controls</v-list-subheader>
      <v-list-item
        v-for="item in userControls"
        :key="item.value"
        :subtitle="item.subtitle"
        :title="item.title"
      ></v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list
      v-model:selected="settingsSelection"
      lines="three"
      select-strategy="leaf"
    >
      <v-list-subheader>General</v-list-subheader>
      <v-list-item
        v-for="item in settingsItems"
        :key="item.value"
        :subtitle="item.subtitle"
        :title="item.title"
        :value="item.value"
      >
        <template v-slot:prepend="{ isSelected, select }">
          <v-list-item-action start>
            <v-checkbox-btn :model-value="isSelected" @update:model-value="select"></v-checkbox-btn>
          </v-list-item-action>
        </template>
      </v-list-item>
    </v-list>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const drawer = ref(null)

const userControls = ref([
  { title: 'Notificações', subtitle: 'Controlar alertas', value: 'notif' },
  { title: 'Sincronização', subtitle: 'Sincronizar dados automaticamente', value: 'sync' },
])

const settingsItems = ref([
  { title: 'Modo Escuro', subtitle: 'Ativar o modo escuro', value: 'dark' },
  { title: 'Idioma', subtitle: 'Selecionar idioma do app', value: 'lang' },
])

const settingsSelection = ref([])
</script>