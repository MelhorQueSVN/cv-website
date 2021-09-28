<template>
    <div> 
    
        <!-- Skills -->
        <v-row> 
          <v-col class="text-left"> 
              <h4> Skills and Main Expertize </h4>
          </v-col>
        </v-row> 
        
        <!-- Consoante o tamanho do ecrã muda o width -->
        <v-divider v-if="$vuetify.breakpoint.smAndDown" width="70%" > </v-divider> 
        <v-divider v-else width="25%" > </v-divider> 
        
        <!-- Em ecrãs pequenos cada coluna ocupa o tamanho todo, em ecrãs maiores ocupa 50%-->
        <v-row class="pt-6 text-left"> 
          
          <v-col cols="12" md="6">
              <p> Java </p>
              <v-progress-linear color="red" height="25" :value="valueJava"> <strong class="aboutMeTextColor"> {{valueJava + "%"}} </strong> </v-progress-linear>
          </v-col> 
          
          <v-col cols="12" md="6"> 
              <p> Javascript </p>
               <v-progress-linear color="yellow accent-3" height="25" :value="valueJavascript"> <strong class="aboutMeTextColor"> {{valueJavascript + "%"}} </strong> </v-progress-linear>                         
          </v-col>
          
          <v-col cols="12" md="6"> 
              <p> VueJs </p>
               <v-progress-linear color="green" height="25" :value="valueVueJs"> <strong class="aboutMeTextColor"> {{valueVueJs + "%"}} </strong> </v-progress-linear>                         
          </v-col>
         
          <v-col cols="12" md="6"> 
              <p> React Native </p>
               <v-progress-linear color="light-blue" height="25" :value="valueReactN"> <strong class="aboutMeTextColor"> {{valueReactN + "%"}} </strong> </v-progress-linear>                         
          </v-col>
         
          <v-col cols="12" md="6"> 
              <p> NodeJs </p>
               <v-progress-linear color="green lighten-2" height="25" :value="valueNodeJs"> <strong class="aboutMeTextColor"> {{valueNodeJs + "%"}} </strong> </v-progress-linear>                         
          </v-col>
         
          <v-col cols="12" md="6"> 
              <p> Python </p>
               <v-progress-linear color="blue darken-4" height="25" :value="valuePython"> <strong class="aboutMeTextColor"> {{valuePython + "%"}} </strong> </v-progress-linear>                         
          </v-col>
          
          <v-col cols="12" md="6"> 
              <p> C/C++ </p>
               <v-progress-linear height="25" :value="valueC"> <strong class="aboutMeTextColor"> {{valueC + "%"}} </strong> </v-progress-linear>                         
          </v-col>
          
          <v-col cols="12" md="6"> 
              <p> Cypher </p>
               <v-progress-linear height="25" :value="valueCy"> <strong class="aboutMeTextColor"> {{valueCy + "%"}} </strong> </v-progress-linear>                         
          </v-col>
          
          <v-col cols="12" md="6"> 
              <p> Mongo </p>
               <v-progress-linear color="green" height="25" :value="valueMongo"> <strong class="aboutMeTextColor"> {{valueMongo + "%"}} </strong> </v-progress-linear>                         
          </v-col>
          
          <v-col cols="12" md="6"> 
              <p> Sql </p>
               <v-progress-linear color="orange lighten-2" height="25" :value="valueSql"> <strong class="aboutMeTextColor"> {{valueSql + "%"}} </strong> </v-progress-linear>                         
          </v-col>
        
        </v-row>      

    </div>
</template>

<script>
export default {

    data() {
        return {

        }
    }

}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>