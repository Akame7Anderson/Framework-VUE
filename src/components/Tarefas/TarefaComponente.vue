<template>
    <div>
      <v-list-item 
    :class="{'deep-orange darken-4':TarefaComponente.concluido}"
    @click="TarefaComponente.concluido = !TarefaComponente.concluido"
    >
      <template v-slot:default="{}">
        <v-list-item-action>
          <v-checkbox :input-value="TarefaComponente.concluido"></v-checkbox>
        </v-list-item-action>

        <v-list-item-content>
          <v-list-item-title
          :class="{'text-decoration-line-through':TarefaComponente.concluido}">{{TarefaComponente.titulo}}</v-list-item-title>
          <v-list-item-subtitle></v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action>
            <v-btn 
            icon
            @click.stop="handleRemoveTarefa(TarefaComponente.id)"
            >
            <v-icon color="red accent-4">mdi-trash-can</v-icon>
            </v-btn>
        </v-list-item-action>
      </template>
    </v-list-item>
    <v-divider></v-divider>
    </div>
</template>

<script>
    
    export default {
      props: ['TarefaComponente'],
      methods:{
        handleRemoveTarefa(id){
          this.$store.commit('removeTarefa', id)
        }
      }
    }

</script>

<style>


</style>