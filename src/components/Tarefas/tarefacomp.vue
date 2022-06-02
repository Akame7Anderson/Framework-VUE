<template>
    <div>
        <v-list-item>
            <template v-slot:default="{ active }">
              <v-list-item-action>
                <v-checkbox :input-value="active"></v-checkbox>
              </v-list-item-action>
  
              <v-list-item-content>
                <v-list-item-title>Notifications</v-list-item-title>
                <v-list-item-subtitle></v-list-item-subtitle>
              </v-list-item-content>
            </template>
          </v-list-item>
    </div>
</template>

<script>
    
    export default {
      name: 'multi-word',

    }





</script>

<style>


</style>