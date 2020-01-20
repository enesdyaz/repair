<template>
  <div>
      <!-- apple, samsung, htc -->
      <v-select v-model="select1" :items='ManufacturerData'></v-select>
      <v-select v-model='select2' :items='ModelData'></v-select>
      <v-select v-model='select3' :items='ProblemData'></v-select>
    <div>
        {{select1}} -- {{select2}} --{{select3}} : {{ValueData}}
    </div>

  </div>

</template>

<script>
export default {
    data(){
        return{
            select1: '',
            select2: '',
            select3: '',
            Manufacturer: {
                apple: {
                    iphone6: {
                        battery: 59,
                        screen: 69,
                    },
                    iphone7: {
                        battery: 39,
                        dock: 48,
                    }
                },
                samsung: {
                    galaxys8: {
                        battery: 49,
                        screen: 120,
                    },
                    galaxys10: {
                        battery: 133,
                        screen: 422,
                    
                    }
                }
            }
        }
    },
    computed: {
        ManufacturerData(){
            return Object.keys(this.Manufacturer)
        },
        ModelData(){
            if(this.select1===''){
                return null
            }else{
                return Object.keys(this.Manufacturer[this.select1])
            }
        },
        ProblemData(){
            if(this.select2===''){
                return null
            }else{
                return Object.keys(this.Manufacturer[this.select1][this.select2])
            }
        },
        ValueData(){
            if(this.select3===''){
                return null
            }else{
                return this.Manufacturer[this.select1][this.select2][this.select3]
            }
        }
    },

}
</script>

<style>


</style>