<template>
    <div>
      

    <v-divider></v-divider>

    <v-list
      flat
      subheader
    >
      <v-subheader>General</v-subheader>

      <v-list-item-group
        v-model="settings"
        multiple
        active-class=""
      >
        <Tarefa />
      </v-list-item-group>
    </v-list>
    </div>
</template>

<script>
  import Tarefa from '../components/Tarefas/tarefacomp.vue'
  export default {
    name: 'multi-word',

    components: {
      Tarefa
    },
  }
</script>
