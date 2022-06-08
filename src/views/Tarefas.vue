<template>
    <div>
      

    <v-divider></v-divider>
    <v-col
          cols="12"
        >
          <v-text-field
            v-model="campoInput"
            solo
            label="Digite alguma tarefa"
            clearable
            @keyup.enter="handleAddTarefa"
          ></v-text-field>
    </v-col>

    <v-list
      flat
      subheader
    >
      <v-subheader>General</v-subheader>

      <v-list-item-group
        multiple
        active-class=""
      >
      <div v-for="TarefaComponente, index in $store.state.tarefas"
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
        campoInput:null,
      }
    },
    methods:{
      handleAddTarefa(){
        this.$store.commit('adicionaTarefa',this.campoInput)
          this.campoInput = null;
        
      }
    }
  }
</script>
