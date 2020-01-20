<template>
  <div>
    <v-container>
      <v-row>
        <v-col col='12' md='4'>
         <phone-model></phone-model>
        </v-col>
        <v-col col='12' md='8'>
          
        </v-col>
      </v-row>
    </v-container>


  </div>
</template>

<script>

import PhoneModel from '../components/PhoneModel.vue'
export default {
  components:{
    PhoneModel,
    
  }
}
</script>

<style>

</style>