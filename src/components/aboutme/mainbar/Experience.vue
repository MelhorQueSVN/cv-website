<template>
    <div> 
    
        <!-- Experience -->
        <v-row> 
          <v-col class="text-left"> 
              <h4> {{ $t('aboutme.mainbar.experience.title') }} </h4>
          </v-col>
        </v-row> 
        
        <!-- Consoante o tamanho do ecrã muda o width -->
        <v-divider v-if="$vuetify.breakpoint.smAndDown" width="30%" > </v-divider> 
        <v-divider v-else width="15%" > </v-divider> 
        
        <v-row class="pt-6"> 
          
          <v-col cols="4" md="2" class="text-left"> 
            <p> 2019-2020 </p>
          </v-col>
          
          <v-col cols="8" md="10" class="text-left"> 
            <p> CeSIUM - Centro de Estudantes da Universidade do Minho </p> 
            <p> {{ $t('aboutme.mainbar.experience.collab') }} </p>
           
            <v-col class="mt-0 pt-0"> 
              <p> &#8226; {{ $t('aboutme.mainbar.experience.first_expl') }} </p>
              <p> &#8226; {{ $t('aboutme.mainbar.experience.second_expl') }} </p>
            </v-col>
          
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