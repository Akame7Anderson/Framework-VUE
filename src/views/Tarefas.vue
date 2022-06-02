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
      <div v-for="TarefaComponente, index in tarefas"
      :key="index"
      >
        <TarefaComponente
          :TarefaComponente="TarefaComponente"
        />

      </div>
        
      </v-list-item-group>
    </v-list>
    </div>
</template>

<script>
  import TarefaComponente from '../components/Tarefas/TarefaComponente.vue'
  export default {
    name: 'multi-word',

    components: {
      TarefaComponente
    },
    data(){
      return{
        tarefas:[
          {titulo:"Ir ao mercado", concluido:false},
        ]
      }
    }
  }
</script>
