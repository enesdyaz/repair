<template>
  <div>
      
     <v-row justify="center">
     <v-dialog v-model="dialog" persistent max-width="600px">
         <template v-slot:activator="{ on }">
         <v-btn color="primary" dark v-on="on">Phone Detail</v-btn>
        </template>

      <v-card>
        <v-card-title>
          <span class="headline">Phone Profile</span>
        </v-card-title>
        <v-card-text>
         
            <v-row>
              <v-col cols="12" sm="6" md="4">
                 <v-select v-model='select1' :items="model" return-object item-text="manufacturer" outlined dense ></v-select>
              </v-col>

              <v-col cols="12" sm="6" md="4">
                     <div v-if="select1 == 'apple' ">
                      <v-select v-model='select2' :items="apple" outlined dense></v-select>
                    </div>
                    
                    <div v-if="select1 == 'samsung'">
                        <v-select v-model='select2' :items="samsung" outlined dense></v-select>
                    </div>
                    <div v-if="select1 == 'htc'">
                        <v-select v-model='select2' :items="htc" outlined dense></v-select>
                    </div>
              </v-col>

              <v-col cols="12" sm="6" md="4">
                    <div v-if="select2 == 'iphone6'">
                        <v-select  v-model='select3'  :items = "iphone6" return-object item-text="problem" outlined dense></v-select>
                    </div>
                    <div v-if="select2 == 'iphone7'">
                        <v-select  v-model='select3'  :items = "iphone7" return-object item-text="problem" outlined dense></v-select>
                    </div>
                    <div v-if="select2 == 'iphone8'">
                        <v-select  v-model='select3'  :items = "iphone8" return-object item-text="problem" outlined dense></v-select>
                    </div>


                    <div v-if="select2 == 'GalaxyS8'">
                        <v-select  v-model='select3'  :items = "GalaxyS8" return-object item-text="problem" outlined dense></v-select>
                    </div>
                    <div v-if="select2 == 'GalaxyS9'">
                        <v-select  v-model='select3'  :items = "GalaxyS9" return-object item-text="problem" outlined dense></v-select>
                    </div>
                    <div v-if="select2 == 'Note10'">
                        <v-select  v-model='select3'  :items = "Note10" return-object item-text="problem" outlined dense></v-select>
                    </div>


                    <div v-if="select2 == 'htc10'">
                        <v-select  v-model='select3'  :items = "htc10" return-object item-text="problem" outlined dense></v-select>
                    </div>
                    <div v-if="select2 == 'htc11'">
                        <v-select  v-model='select3'  :items = "htc11" return-object item-text="problem" outlined dense></v-select>
                    </div>

              </v-col>
            </v-row>
              
          <small>*indicates required field</small>
        </v-card-text>
      
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue darken-1" text @click="dialog = false">Close</v-btn>
          <v-btn color="blue darken-1" text @click="dialog = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>

        <div v-if="select3">
            {{select1}}--{{select2}}--{{select3.problem}} : {{select3.value}}
        </div>
      
  
  </div>
</template>
<script>

export default {
    data(){
        return{
            dialog: false,
            select1: '',
            select2: '',
            select3: '',

            // First Select
            model: ['apple', 'samsung', 'htc'],

            // Second Select
            apple: ['iphone6', 'iphone7', 'iphone8'],
            samsung: ['GalaxyS8', 'GalaxyS9', 'Note10'],
            htc: ['htc10', 'htc11'],

            // Third Select
            iphone6: [ 
                        {problem: 'battery', value: 59}, 
                        {problem: 'screen', value: 79},
                        {problem: 'dockconnector', value: 89},
            ],
            iphone7: [ 
                        {problem: 'battery', value: 159}, 
                        {problem: 'screen', value: 179},
                        {problem: 'dockconnector', value: 189},
            ],
            iphone8: [ 
                        {problem: 'battery', value: 259}, 
                        {problem: 'screen', value: 29},
                        {problem: 'dockconnector', value: 289},
            ],

            GalaxyS8: [ 
                        {problem: 'battery', value: 259}, 
                        {problem: 'screen', value: 29},
                        {problem: 'dockconnector', value: 289},
            ],

            GalaxyS9: [ 
                        {problem: 'battery', value: 259}, 
                        {problem: 'screen', value: 29},
                        {problem: 'dockconnector', value: 289},
            ],

            Note10: [ 
                        {problem: 'battery', value: 259}, 
                        {problem: 'screen', value: 29},
                        {problem: 'dockconnector', value: 289},
            ],

             htc10: [ 
                        {problem: 'battery', value: 259}, 
                        {problem: 'screen', value: 29},
                        {problem: 'dockconnector', value: 289},
            ],

             htc11: [ 
                        {problem: 'battery', value: 259}, 
                        {problem: 'screen', value: 29},
                        {problem: 'dockconnector', value: 289},
            ],
           
        }
    },
   
}
</script>

<style>

</style>