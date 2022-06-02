<template>
    <div>
      

    <v-divider></v-divider>
    <v-col
          cols="12"
          sm="6"
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
        campoInput:'null',
        tarefas:[
          {titulo:"Ir ao mercado", concluido:false},
          {titulo:"Comprar ração", concluido:false},
        ]
      }
    },
    methods:{
      handleAddTarefa(){
        if(this.campoInput){
          this.tarefas.push({
            titulo:this.campoInput,
            concluido:false
          })
          this.campoInput = null;
        }
      }
    }
  }
</script>
