<template>
  <div>
    <v-container>
      <v-row>
        <v-col col='12' md='4'>
         <phone-model></phone-model>
        </v-col>
        <v-col col='12' md='8'>
          <phone-list></phone-list>
        </v-col>
      </v-row>
    </v-container>


  </div>
</template>

<script>

import PhoneModel from '../components/PhoneModel.vue'
import PhoneList from '../components/PhoneList.vue'
export default {
  components:{
    PhoneModel,
    PhoneList
    
  }
}
</script>

<style>

</style>