<template>
    <div>    
        <!-- Educação -->
        <v-row> 
          <v-col class="text-left"> 
              <h4> {{ $t('aboutme.mainbar.education.title') }} </h4>
          </v-col>
        </v-row> 
        
        <!-- Consoante o tamanho do ecrã muda o width -->
        <v-divider v-if="$vuetify.breakpoint.smAndDown" width="30%" > </v-divider> 
        <v-divider v-else width="15%" > </v-divider> 
        
        <v-row class="pt-6"> 
          
          <v-col cols="4" md="2" class="text-left"> 
            <p> 2016-present </p>
          </v-col>
         
          <v-col cols="8" md="10" class="text-left"> 
            <p> Universidade do Minho </p> 
            <p> {{ $t('aboutme.mainbar.education.degree') }} </p>
          </v-col>                       
        
        </v-row> 
        
        <v-row class="mt-0"> 
         
          <v-col cols="4" md="2" class="text-left"> 
            <p> 2013-2016 </p>
          </v-col>
          
          <v-col cols="8" md="10" class="text-left"> 
            <p> Escola Básica e Secundária de Lustosa </p> 
            <p> {{ $t('aboutme.mainbar.education.course_sec') }} </p>
          </v-col>                   
        
        </v-row> 
    
    </div>  
</template>

<script>
export default {

}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>